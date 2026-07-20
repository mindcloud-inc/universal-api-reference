# Wooxy: List Templates

Finds templates in your Wooxy account.

```
GET https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wooxy `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/list-templates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/list-templates?${params}`, {
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
      "data": {
        "createdAt": "string",
        "html": "string",
        "name": "Ava Chen",
        "subject": "string",
        "templateId": "string",
        "templateSource": "string",
        "updatedAt": "string"
      },
      "limit": 1,
      "offset": 1,
      "result": true,
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data.createdAt` | string |  |
| `data.html` | string |  |
| `data.name` | string |  |
| `data.subject` | string |  |
| `data.templateId` | string |  |
| `data.templateSource` | string |  |
| `data.updatedAt` | string |  |
| `limit` | number |  |
| `offset` | number |  |
| `result` | boolean |  |
| `totalCount` | number |  |

## Native endpoint

Through the native Wooxy API, this operation is `POST v3/template/email/find` (base URL `https://api.wooxy.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

