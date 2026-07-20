# ClickSend SMS: Update SMS Campaign

Updates an existing SMS campaign in ClickSend SMS.

```
PUT https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/update-sms-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickSend SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/update-sms-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sms_campaign_id": 1,
  "listId": 1,
  "name": "Ava Chen",
  "from": "string",
  "body": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/update-sms-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sms_campaign_id": 1,
    "listId": 1,
    "name": "Ava Chen",
    "from": "string",
    "body": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sms_campaign_id` | number | yes | ID of the SMS campaign to update. |
| `listId` | number | yes | Target recipient list ID for the campaign. |
| `name` | string | yes | Campaign name. |
| `from` | string | yes | Sender name or number. |
| `body` | string | yes | SMS message content. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `schedule` | number | no | Unix timestamp for scheduled send. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": "string",
      "customString": {},
      "dateAdded": 1,
      "from": "string",
      "listId": 1,
      "listName": "Ava Chen",
      "name": "Ava Chen",
      "schedule": 1,
      "senders": [
        {
          "recipientCountryCode": "string",
          "senderCountryCode": "string",
          "senderId": "string",
          "senderType": "string"
        }
      ],
      "smsCampaignId": 1,
      "source": {},
      "status": "string",
      "subaccountId": 1,
      "totalCount": 1,
      "unsubscribeLink": 1,
      "urlToShorten": {},
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string |  |
| `customString` | object |  |
| `dateAdded` | number |  |
| `from` | string |  |
| `listId` | number |  |
| `listName` | string |  |
| `name` | string |  |
| `schedule` | number |  |
| `senders[].recipientCountryCode` | string |  |
| `senders[].senderCountryCode` | string |  |
| `senders[].senderId` | string |  |
| `senders[].senderType` | string |  |
| `smsCampaignId` | number |  |
| `source` | object |  |
| `status` | string |  |
| `subaccountId` | number |  |
| `totalCount` | number |  |
| `unsubscribeLink` | number |  |
| `urlToShorten` | object |  |
| `userId` | number |  |

## Native endpoint

Through the native ClickSend SMS API, this operation is `PUT /v3/sms-campaigns/:sms_campaign_id` (base URL `https://rest.clicksend.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-sms-campaign.md) for the provider-specific parameters and requirements.

