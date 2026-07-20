# Constant Contact: Schedule Email Campaign Activity

Schedules an email campaign activity in Constant Contact.

```
POST https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/schedule-email-campaign-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Constant Contact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/schedule-email-campaign-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignActivityId": "91569d46-00e4-4a4d-9a4c-d17d98740d04",
  "scheduledDate": "2026-05-17T16:37:59.091Z or 0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/schedule-email-campaign-activity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignActivityId": "91569d46-00e4-4a4d-9a4c-d17d98740d04",
    "scheduledDate": "2026-05-17T16:37:59.091Z or 0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignActivityId` | string | yes | The unique ID for the email campaign activity to schedule. Example: `91569d46-00e4-4a4d-9a4c-d17d98740d04`. |
| `scheduledDate` | string | yes | ISO-8601 send datetime, or "0" to send immediately. Example: `2026-05-17T16:37:59.091Z or 0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "scheduledDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `scheduledDate` | date |  |

## Native endpoint

Through the native Constant Contact API, this operation is `POST /emails/activities/:campaign_activity_id/schedules` (base URL `https://api.cc.email/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/schedule-email-campaign-activity.md) for the provider-specific parameters and requirements.

