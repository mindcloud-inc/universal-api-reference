# ClickSend SMS: Cancel SMS Campaign

Cancels an existing SMS campaign in ClickSend SMS.

```
PUT https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/cancel-sms-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickSend SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/cancel-sms-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sms_campaign_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/cancel-sms-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sms_campaign_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sms_campaign_id` | number | yes | ID of the SMS campaign to cancel. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
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
        "status": "string",
        "subaccountId": 1,
        "totalCount": 1,
        "unsubscribeLink": 1,
        "userId": 1
      },
      "httpCode": 1,
      "responseCode": "string",
      "responseMsg": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.body` | string |  |
| `data.dateAdded` | number |  |
| `data.from` | string |  |
| `data.listId` | number |  |
| `data.listName` | string |  |
| `data.name` | string |  |
| `data.schedule` | number |  |
| `data.senders[].recipientCountryCode` | string |  |
| `data.senders[].senderCountryCode` | string |  |
| `data.senders[].senderId` | string |  |
| `data.senders[].senderType` | string |  |
| `data.smsCampaignId` | number |  |
| `data.status` | string |  |
| `data.subaccountId` | number |  |
| `data.totalCount` | number |  |
| `data.unsubscribeLink` | number |  |
| `data.userId` | number |  |
| `httpCode` | number |  |
| `responseCode` | string |  |
| `responseMsg` | string |  |

## Native endpoint

Through the native ClickSend SMS API, this operation is `PUT /v3/sms-campaigns/:sms_campaign_id/cancel` (base URL `https://rest.clicksend.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-sms-campaign.md) for the provider-specific parameters and requirements.

