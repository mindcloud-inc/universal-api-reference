# Let's Calendar: Update Campaign

Updates an existing campaign in Let's Calendar.

```
PUT https://connect.mindcloud.co/v1/universal/letsCalendar/latest/actions/update-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Let's Calendar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/letsCalendar/latest/actions/update-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "string",
  "title": "string",
  "subject": "string",
  "eventType": "string",
  "senderEmailId": 1,
  "startDate": "string",
  "startTime": "string",
  "endDate": "string",
  "endTime": "string",
  "timezone": "string",
  "description": "string",
  "emailContent": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/letsCalendar/latest/actions/update-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "string",
    "title": "string",
    "subject": "string",
    "eventType": "string",
    "senderEmailId": 1,
    "startDate": "string",
    "startTime": "string",
    "endDate": "string",
    "endTime": "string",
    "timezone": "string",
    "description": "string",
    "emailContent": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | string | yes | The unique identifier of the campaign to update. |
| `title` | string | yes | The title of the campaign. |
| `subject` | string | yes | The email subject line. |
| `eventType` | string | yes | Type of event: online, offline, or physical. |
| `senderEmailId` | number | yes | ID of the sender email to use. |
| `startDate` | string | yes | Start date in Y-m-d format. |
| `startTime` | string | yes | Start time in H:i format. |
| `endDate` | string | yes | End date in Y-m-d format. |
| `endTime` | string | yes | End time in H:i format. |
| `timezone` | string | yes | Timezone for the event. |
| `description` | string | yes | Description of the campaign. |
| `emailContent` | string | yes | HTML content for the invite email body. |
| `location` | string | no | Physical location for the event when the event type is physical. |
| `loginUrl` | string | no | Common login URL for offline events. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaign": {
        "endDatetime": "string",
        "id": "string",
        "startDatetime": "string",
        "timezone": "string",
        "title": "string"
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign.endDatetime` | string |  |
| `campaign.id` | string |  |
| `campaign.startDatetime` | string |  |
| `campaign.timezone` | string |  |
| `campaign.title` | string |  |
| `message` | string |  |

## Native endpoint

Through the native Let's Calendar API, this operation is `PUT campaign/:campaignId` (base URL `https://panel.letscalendar.com/api/lc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-campaign.md) for the provider-specific parameters and requirements.

