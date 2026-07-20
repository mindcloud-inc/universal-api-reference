# Content Snare: List Clients

Retrieves clients from Content Snare.

```
GET https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/list-clients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Content Snare `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/list-clients?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/list-clients?${params}`, {
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
| `includeExternal` | boolean | no | Specifies whether to return clients from external sources (integrations) (include_external=true) |
| `q` | string | no | String to search in the values specified in the parameter `q_by[]` |
| `qBy[]` | array<string> | no | Specifies list of values where string from the parameter `q` will be searched. If it isn't set then the default list is used.<br><b>Examples:</b> q_by[]=email&q_by[]=full_name |
| `sortBy` | string | no | Specifies value for sorting |
| `sortDirection` | string | no | Specifies direction for sorting |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatar": "string",
      "client_companies": [
        {
          "id": "string",
          "name": "Ava Chen"
        }
      ],
      "company_name": "Ava Chen",
      "email": "ava@example.com",
      "first_name": "Ava",
      "full_name": "Ava Chen",
      "id": "string",
      "language_code": "string",
      "last_name": "Chen",
      "phone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar` | string |  |
| `client_companies[].id` | string |  |
| `client_companies[].name` | string |  |
| `company_name` | string |  |
| `email` | string |  |
| `first_name` | string |  |
| `full_name` | string |  |
| `id` | string |  |
| `language_code` | string |  |
| `last_name` | string |  |
| `phone` | string |  |

## Native endpoint

Through the native Content Snare API, this operation is `GET /partner_api/v1/clients` (base URL `https://api.contentsnare.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-clients.md) for the provider-specific parameters and requirements.

