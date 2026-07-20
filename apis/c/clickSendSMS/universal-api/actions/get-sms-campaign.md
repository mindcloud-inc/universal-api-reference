# ClickSend SMS: Get SMS Campaign

Retrieves an SMS campaign from ClickSend SMS.

```
GET https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/get-sms-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickSend SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/get-sms-campaign?connectionId=$CONNECTION_ID&sms_campaign_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sms_campaign_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/get-sms-campaign?${params}`, {
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
| `sms_campaign_id` | string | yes |  |

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

Through the native ClickSend SMS API, this operation is `GET /v3/sms-campaigns/:sms_campaign_id` (base URL `https://rest.clicksend.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sms-campaign.md) for the provider-specific parameters and requirements.

