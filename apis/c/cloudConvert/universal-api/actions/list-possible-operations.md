# CloudConvert: List Possible Operations

Retrieves available file operations from CloudConvert.

```
GET https://connect.mindcloud.co/v1/universal/cloudConvert/latest/actions/list-possible-operations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CloudConvert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudConvert/latest/actions/list-possible-operations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudConvert/latest/actions/list-possible-operations?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "credits": 1,
      "engine": "string",
      "inputFormat": "string",
      "meta": {
        "group": "string"
      },
      "operation": "string",
      "outputFormat": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credits` | number |  |
| `engine` | string |  |
| `inputFormat` | string |  |
| `meta.group` | string |  |
| `operation` | string |  |
| `outputFormat` | string |  |

## Native endpoint

Through the native CloudConvert API, this operation is `GET /operations` (base URL `https://api.cloudconvert.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-possible-operations.md) for the provider-specific parameters and requirements.

