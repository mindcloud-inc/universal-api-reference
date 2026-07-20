# FileCloud: List Schemas

Retrieves schemas from FileCloud.

```
GET https://connect.mindcloud.co/v1/universal/fileCloud/latest/actions/list-schemas
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FileCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fileCloud/latest/actions/list-schemas?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fileCloud/latest/actions/list-schemas?${params}`, {
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
      "Resources": [
        {}
      ],
      "schemas": [
        "string"
      ],
      "totalResults": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Resources` | array<object> |  |
| `schemas` | array<string> |  |
| `totalResults` | number |  |

## Native endpoint

Through the native FileCloud API, this operation is `GET /scim/Schemas` (base URL `https://mindcloud.filecloudtrial.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-schemas.md) for the provider-specific parameters and requirements.

