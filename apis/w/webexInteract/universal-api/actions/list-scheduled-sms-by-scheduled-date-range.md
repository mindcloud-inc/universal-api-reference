# Webex Interact: List scheduled SMS by scheduled date range

Finds scheduled SMS requests in Webex Interact by scheduled date range.

```
GET https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/list-scheduled-sms-by-scheduled-date-range
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webex Interact `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/list-scheduled-sms-by-scheduled-date-range?connectionId=$CONNECTION_ID&limit=25&offset=0&scheduled_at_end=2026-05-07T12%3A00%3A00.000Z&scheduled_at_start=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "scheduled_at_end": "2026-05-07T12:00:00.000Z",
  "scheduled_at_start": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/list-scheduled-sms-by-scheduled-date-range?${params}`, {
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
| `name` | string | no | Fuzzy match search on the campaign or API request name. |
| `page_number` | string | no | Page number for scheduled SMS results. |
| `page_size` | string | no | Number of scheduled SMS results to return per page. |
| `request_types` | list<string> | no | Optional request types to include. Accepts multiple values as an array. |
| `scheduled_at_end` | date | yes | End of the scheduled send time range. |
| `scheduled_at_start` | date | yes | Start of the scheduled send time range. |
| `sort_by` | string | no | Scheduled SMS sort field such as created_at, updated_at, scheduled_at, name, or status. |
| `sort_order` | string | no | Sort order, ASC or DESC. |
| `status` | list<string> | no | Optional scheduled request statuses to include. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "items": [
        {}
      ],
      "name": "Ava Chen",
      "paging": {},
      "scheduled_at": "2026-05-07T12:00:00.000Z",
      "sender_name": "Ava Chen",
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Scheduled request ID. |
| `items` | array<object> | Scheduled SMS requests matching the scheduled date range. |
| `name` | string | Scheduled request name. |
| `paging` | object | Paging metadata for the scheduled SMS result set. |
| `scheduled_at` | date | Scheduled send time. |
| `sender_name` | string | Sender name used for the scheduled request. |
| `status` | string | Scheduled request status. |
| `type` | string | Scheduled request type. |

## Native endpoint

Through the native Webex Interact API, this operation is `POST /campaigns/v1/scheduled` (base URL `https://api.webexinteract.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-scheduled-sms-by-scheduled-date-range.md) for the provider-specific parameters and requirements.

