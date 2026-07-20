# Pitchbox: Get Campaign Outreach Settings



```
GET https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/get-campaign-outreach-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pitchbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/get-campaign-outreach-settings?connectionId=$CONNECTION_ID&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/get-campaign-outreach-settings?${params}`, {
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
| `campaignId` | string | yes | Pitchbox campaign identifier |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaign": {
        "id": 1,
        "name": "Ava Chen",
        "status": "string"
      },
      "dailyLimit": 1,
      "isActive": true,
      "pauseOutreachUntil": "2026-05-07T12:00:00.000Z",
      "schedule": {
        "friday": true,
        "monday": true,
        "saturday": true,
        "sunday": true,
        "thursday": true,
        "tuesday": true,
        "wednesday": true
      },
      "scheduleTimeFrom": "string",
      "scheduleTimeTo": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign.id` | number |  |
| `campaign.name` | string |  |
| `campaign.status` | string |  |
| `dailyLimit` | number |  |
| `isActive` | boolean |  |
| `pauseOutreachUntil` | date |  |
| `schedule.friday` | boolean |  |
| `schedule.monday` | boolean |  |
| `schedule.saturday` | boolean |  |
| `schedule.sunday` | boolean |  |
| `schedule.thursday` | boolean |  |
| `schedule.tuesday` | boolean |  |
| `schedule.wednesday` | boolean |  |
| `scheduleTimeFrom` | string |  |
| `scheduleTimeTo` | string |  |

## Native endpoint

Through the native Pitchbox API, this operation is `GET /api/campaigns/:campaignId/outreach_settings` (base URL `https://apiv2.pitchbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-outreach-settings.md) for the provider-specific parameters and requirements.

