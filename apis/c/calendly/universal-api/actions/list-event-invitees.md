# Calendly: List Event Invitees

Retrieves invitees for a Calendly event.

```
GET https://connect.mindcloud.co/v1/universal/calendly/latest/actions/list-event-invitees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calendly `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calendly/latest/actions/list-event-invitees?connectionId=$CONNECTION_ID&limit=25&offset=0&event_uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "event_uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calendly/latest/actions/list-event-invitees?${params}`, {
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
| `event_uuid` | string | yes | Scheduled event UUID. |
| `status` | list | no | Invitee status filter. One of: `active`, `canceled`. |
| `email` | string | no | Filter invitees by email address. |
| `sort` | list | no | Sort order for event invitees. One of: `created_at:asc`, `created_at:desc`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "collection": [
        {}
      ],
      "pagination": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `collection` | array<object> | Invitee records for the scheduled event. |
| `pagination` | object | Pagination metadata for invitees. |

## Native endpoint

Through the native Calendly API, this operation is `GET /scheduled_events/:event_uuid/invitees` (base URL `https://api.calendly.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-event-invitees.md) for the provider-specific parameters and requirements.

