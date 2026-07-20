# Zoho Writer: List Fillable Templates

Retrieves fillable templates from Zoho Writer.

```
GET https://connect.mindcloud.co/v1/universal/zohoWriter/latest/actions/list-fillable-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Writer `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoWriter/latest/actions/list-fillable-templates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoWriter/latest/actions/list-fillable-templates?${params}`, {
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
      "documents": [
        {
          "id": "string",
          "name": "Ava Chen",
          "status": "string",
          "type": "string"
        }
      ],
      "limit": 1,
      "message": "string",
      "offset": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documents` | array<object> |  |
| `documents[].id` | string |  |
| `documents[].name` | string |  |
| `documents[].status` | string |  |
| `documents[].type` | string |  |
| `limit` | number |  |
| `message` | string |  |
| `offset` | number |  |

## Native endpoint

Through the native Zoho Writer API, this operation is `GET /v1/documents` (base URL `{{credentials.accessTokenRequest.api_domain}}/writer/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-fillable-templates.md) for the provider-specific parameters and requirements.

