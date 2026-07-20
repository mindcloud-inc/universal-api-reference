# MailerLite: Get Automation Subscriber Activity

Retrieves subscriber activity for an automation in MailerLite.

```
GET https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/get-automation-subscriber-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailerLite `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/get-automation-subscriber-activity?connectionId=$CONNECTION_ID&limit=25&offset=0&automationId=123456789&filter%5Bstatus%5D=completed" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "automationId": "123456789",
  "filter[status]": "completed"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/get-automation-subscriber-activity?${params}`, {
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
| `automationId` | string | yes | MailerLite automation ID. Example: `123456789`. |
| `filter[status]` | string | yes | Activity status: completed, active, canceled, or failed. Example: `completed`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filter[date_from]` | date | no | Start date for completed, canceled, or failed activity. Example: `2026-03-01`. |
| `filter[date_to]` | date | no | End date for completed, canceled, or failed activity. Example: `2026-03-05`. |
| `filter[scheduled_from]` | date | no | Start date for active scheduled activity. Example: `2026-03-01`. |
| `filter[scheduled_to]` | date | no | End date for active scheduled activity. Example: `2026-03-05`. |
| `filter[search]` | string | no | Filter activity by subscriber email address. Example: `user@example.com`. |
| `limit` | number | no | Number of activity rows to return per page. Example: `10`. |
| `page` | number | no | Page number to return. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "links": {
        "first": "https://example.com",
        "last": "https://example.com",
        "next": "https://example.com",
        "prev": "https://example.com"
      },
      "meta": {
        "currentPage": 1,
        "from": 1,
        "lastPage": 1,
        "links": [
          {
            "active": true,
            "label": "https://example.com",
            "url": "https://example.com"
          }
        ],
        "path": "string",
        "perPage": 1,
        "to": 1,
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `links` | object |  |
| `links.first` | string |  |
| `links.last` | string |  |
| `links.next` | string |  |
| `links.prev` | string |  |
| `meta` | object |  |
| `meta.currentPage` | number |  |
| `meta.from` | number |  |
| `meta.lastPage` | number |  |
| `meta.links` | array<object> |  |
| `meta.links[].active` | boolean |  |
| `meta.links[].label` | string |  |
| `meta.links[].url` | string |  |
| `meta.path` | string |  |
| `meta.perPage` | number |  |
| `meta.to` | number |  |
| `meta.total` | number |  |

## Native endpoint

Through the native MailerLite API, this operation is `GET /automations/:automationId/activity` (base URL `https://connect.mailerlite.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-automation-subscriber-activity.md) for the provider-specific parameters and requirements.

