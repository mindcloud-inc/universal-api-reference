# Mailchimp: Schedule Campaign

Schedules a campaign in Mailchimp.

```
PUT https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/schedule-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailchimp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/schedule-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaign_id": "string",
  "schedule_time": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/schedule-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaign_id": "string",
    "schedule_time": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `batch_delivery` | object | no |  |
| `campaign_id` | string | yes | The unique ID for the campaign. |
| `schedule_time` | date | yes | Scheduled send time. |
| `timewarp` | boolean | no | Whether to use Timewarp scheduling. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Mailchimp API returns.

## Native endpoint

Through the native Mailchimp API, this operation is `POST campaigns/:campaign_id/actions/schedule` (base URL `https://{{credentials.serverPrefix}}.api.mailchimp.com/3.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/schedule-campaign.md) for the provider-specific parameters and requirements.

