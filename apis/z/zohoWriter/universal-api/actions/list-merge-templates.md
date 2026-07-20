# Zoho Writer: List Merge Templates

Retrieves merge templates from Zoho Writer.

```
GET https://connect.mindcloud.co/v1/universal/zohoWriter/latest/actions/list-merge-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Writer `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoWriter/latest/actions/list-merge-templates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoWriter/latest/actions/list-merge-templates?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `category` | string | no | Limit results to all templates, templates shared to you, or templates you own. |
| `sortBy` | string | no | Sort merge templates by created time, modified time, or name. |
| `sortOrderBy` | string | no | Choose ascending or descending sort order. |

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

Through the native Zoho Writer API, this operation is `GET /v1/documents` (base URL `{{credentials.accessTokenRequest.api_domain}}/writer/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-merge-templates.md) for the provider-specific parameters and requirements.

