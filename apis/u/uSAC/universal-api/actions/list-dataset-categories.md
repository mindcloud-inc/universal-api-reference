# USAC: List Dataset Categories



```
GET https://connect.mindcloud.co/v1/universal/uSAC/latest/actions/list-dataset-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a USAC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uSAC/latest/actions/list-dataset-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uSAC/latest/actions/list-dataset-categories?${params}`, {
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
      "param": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `param` | string |  |
| `value` | string |  |

## Native endpoint

Through the native USAC API, this operation is `GET api/browse_config` (base URL `https://opendata.usac.org/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-dataset-categories.md) for the provider-specific parameters and requirements.

