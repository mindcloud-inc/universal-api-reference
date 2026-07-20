# Webex Interact: List scheduled SMS by created date range

Finds scheduled SMS requests in Webex Interact by created date range.

```
GET https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/list-scheduled-sms-by-created-date-range
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webex Interact `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/list-scheduled-sms-by-created-date-range?connectionId=$CONNECTION_ID&limit=25&offset=0&created_at_start=2026-05-07T12%3A00%3A00.000Z&created_at_end=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "created_at_start": "2026-05-07T12:00:00.000Z",
  "created_at_end": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/list-scheduled-sms-by-created-date-range?${params}`, {
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
| `id` | string | no | Campaign or API SMS request ID to retrieve. |
| `name` | string | no | Fuzzy match search on the campaign or API request name. |
| `page_number` | string | no | Page number to return. |
| `page_size` | string | no | Number of scheduled requests per page. |
| `scheduled_at_end` | date | no | End of scheduled-at date range. |
| `scheduled_at_start` | date | no | Start of scheduled-at date range. |
| `sort_by` | string | no | Scheduled SMS sort field such as created_at, updated_at, scheduled_at, name, or status. |
| `sort_order` | string | no | Sort order, ASC or DESC. |
| `created_at_start` | date | yes | Start of created-at date range. Required unless ID or scheduled-at range is supplied. |
| `created_at_end` | date | yes | End of created-at date range. Required with created-at start. |
| `status` | list<string> | no | Statuses to return, such as SCHEDULED, SENT, ERROR, DELETED, or IN_PROGRESS. |
| `request_types` | list<string> | no | Request types to return: CAMPAIGN and/or API. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {}
      ],
      "paging": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> |  |
| `paging` | object |  |

## Native endpoint

Through the native Webex Interact API, this operation is `POST /campaigns/v1/scheduled` (base URL `https://api.webexinteract.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-scheduled-sms-by-created-date-range.md) for the provider-specific parameters and requirements.

