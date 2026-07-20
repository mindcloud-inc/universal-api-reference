# Moosend: Schedule Campaign

Schedules a campaign in Moosend.

```
PUT https://connect.mindcloud.co/v1/universal/moosend/latest/actions/schedule-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moosend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/moosend/latest/actions/schedule-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "string",
  "dateTime": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moosend/latest/actions/schedule-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "string",
    "dateTime": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | string | yes | The ID of the campaign that you want to schedule. |
| `dateTime` | date | yes | The specific date and time the campaign is scheduled to be delivered. Use the same format that you have in the Time and date settings in your account. For example, dd-mm-yyyy . |
| `timezone` | string | no | The time zone of your specified date and time. If you don't specify any timezone value , the time zone in your time and date settings is used. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Moosend API returns.

## Native endpoint

Through the native Moosend API, this operation is `POST /campaigns/{{CampaignID}}/schedule.json` (base URL `https://api.moosend.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/schedule-campaign.md) for the provider-specific parameters and requirements.

