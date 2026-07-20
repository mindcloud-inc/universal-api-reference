# Infobip: Get Inbound SMS Messages



```
GET https://connect.mindcloud.co/v1/universal/infobip/latest/actions/get-inbound-sms-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infobip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/infobip/latest/actions/get-inbound-sms-messages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/infobip/latest/actions/get-inbound-sms-messages?${params}`, {
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
| `limit` | number | no | Maximum number of messages to be returned in a response. If not set, the latest 50 records are returned. Maximum limit value is `1000` and you can only access messages for the last 48h. |
| `applicationId` | string | no | Application id that the message is linked to. For more details, see our [documentation](https://www.infobip.com/docs/cpaas-x/application-and-entity-management). |
| `entityId` | string | no | Entity id that the message is linked to. For more details, see our [documentation](https://www.infobip.com/docs/cpaas-x/application-and-entity-management). |
| `campaignReferenceId` | string | no | ID of a campaign that was sent in the message. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "messageCount": 1,
      "pendingMessageCount": 1,
      "results": {
        "applicationId": "string",
        "callbackData": "string",
        "campaignReferenceId": "string",
        "cleanText": "string",
        "entityId": "string",
        "from": "string",
        "keyword": "string",
        "messageId": "string",
        "price": {
          "currency": "string",
          "pricePerMessage": 1
        },
        "receivedAt": "2026-05-07T12:00:00.000Z",
        "smsCount": 1,
        "text": "string",
        "to": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `messageCount` | number |  |
| `pendingMessageCount` | number |  |
| `results` | array<object> |  |
| `results.applicationId` | string |  |
| `results.callbackData` | string |  |
| `results.campaignReferenceId` | string |  |
| `results.cleanText` | string |  |
| `results.entityId` | string |  |
| `results.from` | string |  |
| `results.keyword` | string |  |
| `results.messageId` | string |  |
| `results.price` | object |  |
| `results.price.currency` | string |  |
| `results.price.pricePerMessage` | number |  |
| `results.receivedAt` | date |  |
| `results.smsCount` | number |  |
| `results.text` | string |  |
| `results.to` | string |  |

## Native endpoint

Through the native Infobip API, this operation is `GET /sms/1/inbox/reports` (base URL `https://rkpzwe.api.infobip.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-inbound-sms-messages.md) for the provider-specific parameters and requirements.

