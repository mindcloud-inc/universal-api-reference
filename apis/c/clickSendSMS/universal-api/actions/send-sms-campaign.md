# ClickSend SMS: Send SMS Campaign

Creates and sends an SMS campaign in ClickSend SMS.

```
POST https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/send-sms-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickSend SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/send-sms-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "list_id": 1,
  "name": "Ava Chen",
  "from": "string",
  "body": "string",
  "senders": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/send-sms-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "list_id": 1,
    "name": "Ava Chen",
    "from": "string",
    "body": "string",
    "senders": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `list_id` | number | yes |  |
| `name` | string | yes |  |
| `from` | string | yes |  |
| `body` | string | yes |  |
| `senders` | list<object> | yes |  |
| `senders[].recipient_country_code` | string | no |  |
| `senders[].sender_id` | string | no |  |
| `senders[].sender_type` | string | no |  |
| `senders[].sender_country_code` | string | no |  |
| `source` | string | no |  |
| `schedule` | number | no |  |
| `url_to_shorten` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "smsCampaign": {
        "body": "string",
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
        "userId": 1
      },
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `smsCampaign.body` | string |  |
| `smsCampaign.dateAdded` | number |  |
| `smsCampaign.from` | string |  |
| `smsCampaign.listId` | number |  |
| `smsCampaign.listName` | string |  |
| `smsCampaign.name` | string |  |
| `smsCampaign.schedule` | number |  |
| `smsCampaign.senders[].recipientCountryCode` | string |  |
| `smsCampaign.senders[].senderCountryCode` | string |  |
| `smsCampaign.senders[].senderId` | string |  |
| `smsCampaign.senders[].senderType` | string |  |
| `smsCampaign.smsCampaignId` | number |  |
| `smsCampaign.source` | object |  |
| `smsCampaign.status` | string |  |
| `smsCampaign.subaccountId` | number |  |
| `smsCampaign.totalCount` | number |  |
| `smsCampaign.unsubscribeLink` | number |  |
| `smsCampaign.userId` | number |  |
| `totalCount` | number |  |

## Native endpoint

Through the native ClickSend SMS API, this operation is `POST /v3/sms-campaigns/send` (base URL `https://rest.clicksend.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-sms-campaign.md) for the provider-specific parameters and requirements.

