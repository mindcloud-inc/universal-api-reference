# ClickSend SMS: Get Inbound SMS

Retrieves an inbound SMS message from ClickSend SMS.

```
GET https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/get-inbound-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickSend SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/get-inbound-sms?connectionId=$CONNECTION_ID&originalMessageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "originalMessageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/get-inbound-sms?${params}`, {
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
| `originalMessageId` | string | yes | Original inbound message identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "body": "string",
        "customString": "string",
        "from": "string",
        "keyword": "string",
        "messageId": "string",
        "originalBody": "string",
        "originalMessageId": "string",
        "timestamp": 1,
        "to": "string"
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
| `data.body` | string | Inbound SMS body. |
| `data.customString` | string | Custom note attached to the inbound SMS. |
| `data.from` | string | Phone number that sent the inbound SMS. |
| `data.keyword` | string | Deprecated keyword field derived from the first word of the inbound body. |
| `data.messageId` | string | Inbound SMS message identifier. |
| `data.originalBody` | string | Last message body sent before the inbound reply. |
| `data.originalMessageId` | string | ID of the original outbound message. |
| `data.timestamp` | number | Unix timestamp when the inbound SMS was received. |
| `data.to` | string | Receiving ClickSend number. |
| `httpCode` | number | HTTP code returned by ClickSend. |
| `responseCode` | string | ClickSend response code. |
| `responseMsg` | string | Outcome message for the inbound SMS lookup. |

## Native endpoint

Through the native ClickSend SMS API, this operation is `GET /v3/sms/inbound/:original_message_id` (base URL `https://rest.clicksend.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-inbound-sms.md) for the provider-specific parameters and requirements.

