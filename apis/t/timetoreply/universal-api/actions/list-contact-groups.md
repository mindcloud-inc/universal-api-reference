# Timetoreply: List Contact Groups



```
GET https://connect.mindcloud.co/v1/universal/timetoreply/latest/actions/list-contact-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timetoreply `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timetoreply/latest/actions/list-contact-groups?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timetoreply/latest/actions/list-contact-groups?${params}`, {
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
| `search` | string | no | Filter contact groups by a search term. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company_id": 1,
      "crm_type": "string",
      "customer_domains": [
        "string"
      ],
      "customer_emails": [
        "ava@example.com"
      ],
      "id": 1,
      "name": "Ava Chen",
      "search_string": "string",
      "user_permissions": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company_id` | number |  |
| `crm_type` | string |  |
| `customer_domains` | array |  |
| `customer_emails` | array |  |
| `id` | number |  |
| `name` | string |  |
| `search_string` | string |  |
| `user_permissions` | array |  |

## Native endpoint

Through the native Timetoreply API, this operation is `GET /api/entities/contact-groups` (base URL `https://portal.timetoreply.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contact-groups.md) for the provider-specific parameters and requirements.

