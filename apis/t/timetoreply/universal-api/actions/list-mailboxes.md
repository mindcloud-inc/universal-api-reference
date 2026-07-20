# Timetoreply: List Mailboxes



```
GET https://connect.mindcloud.co/v1/universal/timetoreply/latest/actions/list-mailboxes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timetoreply `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timetoreply/latest/actions/list-mailboxes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timetoreply/latest/actions/list-mailboxes?${params}`, {
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
| `search` | string | no | Filter mailboxes by a search term. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "business_hours": [
        "string"
      ],
      "company_id": 1,
      "company_name": "Ava Chen",
      "created_at": "string",
      "email": "ava@example.com",
      "email_usernames": [
        "ava@example.com"
      ],
      "id": 1,
      "ingestion_completed_date": "string",
      "ingestion_duration": "string",
      "ingestion_duration_seconds": 1,
      "ingestion_started_date": "string",
      "is_bulk_linked": true,
      "is_user": true,
      "last_used_addon": "string",
      "leave_days": [
        "string"
      ],
      "main_type": "string",
      "name": "Ava Chen",
      "newest_message_date": "string",
      "opted_into_body_ingestion": true,
      "search_string": "string",
      "timezone": "string",
      "ttr_extension_installed": true,
      "user_permissions": [
        "string"
      ],
      "work_days": [
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
| `active` | boolean |  |
| `business_hours` | array |  |
| `company_id` | number |  |
| `company_name` | string |  |
| `created_at` | string |  |
| `email` | string |  |
| `email_usernames` | array |  |
| `id` | number |  |
| `ingestion_completed_date` | string |  |
| `ingestion_duration` | string |  |
| `ingestion_duration_seconds` | number |  |
| `ingestion_started_date` | string |  |
| `is_bulk_linked` | boolean |  |
| `is_user` | boolean |  |
| `last_used_addon` | string |  |
| `leave_days` | array |  |
| `main_type` | string |  |
| `name` | string |  |
| `newest_message_date` | string |  |
| `opted_into_body_ingestion` | boolean |  |
| `search_string` | string |  |
| `timezone` | string |  |
| `ttr_extension_installed` | boolean |  |
| `user_permissions` | array |  |
| `work_days` | array |  |

## Native endpoint

Through the native Timetoreply API, this operation is `GET /api/entities/mailboxes` (base URL `https://portal.timetoreply.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-mailboxes.md) for the provider-specific parameters and requirements.

