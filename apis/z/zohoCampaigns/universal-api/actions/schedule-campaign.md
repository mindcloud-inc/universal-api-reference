# Zoho Campaigns: Schedule Campaign

Schedules a campaign in Zoho Campaigns.

```
PUT https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/schedule-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Campaigns `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/schedule-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignKey": "f70c4878c4a47169407e63917ad24497",
  "scheduleDate": "01/19/2027",
  "scheduleHour": "12",
  "scheduleMinute": "15",
  "amPm": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/schedule-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignKey": "f70c4878c4a47169407e63917ad24497",
    "scheduleDate": "01/19/2027",
    "scheduleHour": "12",
    "scheduleMinute": "15",
    "amPm": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignKey` | string | yes | Campaign key from a recent-campaign response. Example: `f70c4878c4a47169407e63917ad24497`. |
| `scheduleDate` | string | yes | Date to schedule the campaign in mm/dd/yyyy format. Example: `01/19/2027`. |
| `scheduleHour` | number | yes | Hour portion of the scheduled send time. Example: `12`. |
| `scheduleMinute` | number | yes | Minute portion of the scheduled send time. Example: `15`. |
| `amPm` | string | yes | Meridiem for the scheduled send time. One of: `0`, `1`. |
| `isTimewarp` | boolean | no | Whether to send in the sender's time zone. |
| `sendingTz` | string | no | Recipient time zone for scheduled sending. Example: `Asia/Kolkata`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignStatus": "string",
      "code": "string",
      "message": "string",
      "uri": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignStatus` | string | Returned scheduling state for the campaign. |
| `code` | string | Zoho result code. |
| `message` | string | Provider message for the scheduling attempt. |
| `uri` | string | Zoho endpoint URI. |
| `version` | string | Zoho API version. |

## Native endpoint

Through the native Zoho Campaigns API, this operation is `POST /sendcampaign` (base URL `https://campaigns.zoho.com/api/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/schedule-campaign.md) for the provider-specific parameters and requirements.

