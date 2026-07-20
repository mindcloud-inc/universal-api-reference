# Calendly: List Scheduled Events

Retrieves scheduled events from Calendly.

```
GET https://connect.mindcloud.co/v1/universal/calendly/latest/actions/list-scheduled-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calendly `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calendly/latest/actions/list-scheduled-events?connectionId=$CONNECTION_ID&limit=25&offset=0&organization=https%3A%2F%2Fapi.calendly.com%2Forganizations%2Fe684df12-9454-43ef-8fc4-2d0faa4ec21e" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organization": "https://api.calendly.com/organizations/e684df12-9454-43ef-8fc4-2d0faa4ec21e"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calendly/latest/actions/list-scheduled-events?${params}`, {
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
| `organization` | list | yes | Organization URI filter. One of: `https://api.calendly.com/organizations/e684df12-9454-43ef-8fc4-2d0faa4ec21e`. Default: `https://api.calendly.com/organizations/e684df12-9454-43ef-8fc4-2d0faa4ec21e`. |
| `user` | list | no | User URI filter. One of: `https://api.calendly.com/users/264e5a40-147f-45f9-a96c-a6f2f0a91dff`. |
| `inviteeEmail` | string | no | Filter scheduled events by invitee email. |
| `status` | list | no | Event status filter. One of: `active`, `canceled`. |
| `group` | string | no | Group URI filter. |
| `sort` | list | no | Sort order for scheduled events. One of: `start_time:asc`, `start_time:desc`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `minStartTime` | date | no | Minimum event start timestamp (ISO-8601). Default: `2026-02-26T00:00:00Z`. |
| `maxStartTime` | date | no | Maximum event start timestamp (ISO-8601). Default: `2026-03-05T00:00:00Z`. |

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
| `collection` | array<object> | Scheduled event records. |
| `pagination` | object | Pagination metadata for scheduled events. |

## Native endpoint

Through the native Calendly API, this operation is `GET /scheduled_events` (base URL `https://api.calendly.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-scheduled-events.md) for the provider-specific parameters and requirements.

