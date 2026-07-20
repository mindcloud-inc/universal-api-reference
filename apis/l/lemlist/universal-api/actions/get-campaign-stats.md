# lemlist: Get Campaign Stats

Retrieves statistics for a lemlist campaign.

```
GET https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/get-campaign-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a lemlist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/get-campaign-stats?connectionId=$CONNECTION_ID&campaignId=67618ad126d28d06429eb1c4&startDate=2025-01-01T00%3A00%3A00.000Z&endDate=2025-01-31T23%3A59%3A59.999Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "67618ad126d28d06429eb1c4",
  "startDate": "2025-01-01T00:00:00.000Z",
  "endDate": "2025-01-31T23:59:59.999Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/get-campaign-stats?${params}`, {
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
| `campaignId` | string | yes | The ID of the campaign to inspect. Example: `67618ad126d28d06429eb1c4`. |
| `startDate` | string | yes | The start of the reporting range in ISO 8601 format. Example: `2025-01-01T00:00:00.000Z`. |
| `endDate` | string | yes | The end of the reporting range in ISO 8601 format. Example: `2025-01-31T23:59:59.999Z`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sendUser` | string | no | Filter statistics to a specific sending user. Example: `usr_123`. |
| `abSelected` | list | no | Return statistics for only the A or B branch. One of: `A`, `B`. Example: `A`. |
| `channels` | string | no | A JSON array string of channels to include. Example: `email,linkedin`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clicked": 1,
      "delivered": 1,
      "invitationAccepted": 1,
      "meetingBooked": 1,
      "messagesBounced": 1,
      "messagesNotSent": 1,
      "messagesSent": 1,
      "nbLeads": 1,
      "nbLeadsAnswered": 1,
      "nbLeadsInteracted": 1,
      "nbLeadsInterested": 1,
      "nbLeadsInterrupted": 1,
      "nbLeadsLaunched": 1,
      "nbLeadsNotInterested": 1,
      "nbLeadsOpened": 1,
      "nbLeadsReached": 1,
      "nbLeadsUnsubscribed": 1,
      "opened": 1,
      "replied": 1,
      "steps": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clicked` | number | Clicked messages. |
| `delivered` | number | Delivered messages. |
| `invitationAccepted` | number | Accepted invitations. |
| `meetingBooked` | number | Meetings booked. |
| `messagesBounced` | number | Messages that bounced. |
| `messagesNotSent` | number | Messages that were not sent. |
| `messagesSent` | number | Messages sent. |
| `nbLeads` | number | Total leads in the campaign during the selected range. |
| `nbLeadsAnswered` | number | Leads who answered the campaign. |
| `nbLeadsInteracted` | number | Leads who interacted with the campaign. |
| `nbLeadsInterested` | number | Leads marked interested. |
| `nbLeadsInterrupted` | number | Leads interrupted from the campaign. |
| `nbLeadsLaunched` | number | Leads launched during the selected range. |
| `nbLeadsNotInterested` | number | Leads marked not interested. |
| `nbLeadsOpened` | number | Leads who opened at least one message. |
| `nbLeadsReached` | number | Leads reached during the selected range. |
| `nbLeadsUnsubscribed` | number | Leads who unsubscribed. |
| `opened` | number | Opened messages. |
| `replied` | number | Replies received. |
| `steps` | array<object> | Step-level statistics. |

## Native endpoint

Through the native lemlist API, this operation is `GET /v2/campaigns/:campaignId/stats` (base URL `https://api.lemlist.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-stats.md) for the provider-specific parameters and requirements.

