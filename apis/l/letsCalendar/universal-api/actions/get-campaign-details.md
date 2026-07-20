# Let's Calendar: Get Campaign Details

Retrieves campaign details from Let's Calendar.

```
GET https://connect.mindcloud.co/v1/universal/letsCalendar/latest/actions/get-campaign-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Let's Calendar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/letsCalendar/latest/actions/get-campaign-details?connectionId=$CONNECTION_ID&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/letsCalendar/latest/actions/get-campaign-details?${params}`, {
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
| `campaignId` | string | yes | The unique identifier of the campaign. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaign": {
        "campaignContent": "string",
        "campaignDescription": "string",
        "campaignId": "string",
        "campaignName": "Ava Chen",
        "campaignSubject": "string",
        "endDatetime": "string",
        "eventType": "string",
        "isRecurring": true,
        "location": "string",
        "mailProvider": "string",
        "mailServiceName": "Ava Chen",
        "senderEmailId": 1,
        "startDatetime": "string",
        "timezone": "string"
      },
      "senderEmails": [
        {
          "disconnected": true,
          "displayText": "ava@example.com",
          "id": 1,
          "provider": "ava@example.com",
          "senderEmail": "ava@example.com",
          "senderName": "ava@example.com"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign.campaignContent` | string |  |
| `campaign.campaignDescription` | string |  |
| `campaign.campaignId` | string |  |
| `campaign.campaignName` | string |  |
| `campaign.campaignSubject` | string |  |
| `campaign.endDatetime` | string |  |
| `campaign.eventType` | string |  |
| `campaign.isRecurring` | boolean |  |
| `campaign.location` | string |  |
| `campaign.mailProvider` | string |  |
| `campaign.mailServiceName` | string |  |
| `campaign.senderEmailId` | number |  |
| `campaign.startDatetime` | string |  |
| `campaign.timezone` | string |  |
| `senderEmails[].disconnected` | boolean |  |
| `senderEmails[].displayText` | string |  |
| `senderEmails[].id` | number |  |
| `senderEmails[].provider` | string |  |
| `senderEmails[].senderEmail` | string |  |
| `senderEmails[].senderName` | string |  |

## Native endpoint

Through the native Let's Calendar API, this operation is `GET campaign/:campaignId/edit` (base URL `https://panel.letscalendar.com/api/lc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-details.md) for the provider-specific parameters and requirements.

