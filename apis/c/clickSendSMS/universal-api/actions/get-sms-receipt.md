# ClickSend SMS: Get SMS Receipt

Retrieves an SMS receipt from ClickSend SMS.

```
GET https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/get-sms-receipt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickSend SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/get-sms-receipt?connectionId=$CONNECTION_ID&message_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "message_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/get-sms-receipt?${params}`, {
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
| `message_id` | string | yes | Message identifier returned by send/history/receipts endpoints. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "customString": "string",
        "digits": 1,
        "errorCode": 1,
        "errorText": "string",
        "messageId": "string",
        "messageType": "string",
        "statusCode": 1,
        "statusText": "string",
        "subaccountId": 1,
        "timestamp": 1,
        "timestampSend": 1
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
| `data.customString` | string | Custom note attached to the original outbound SMS. |
| `data.digits` | number | Voice digits value when the receipt is for a voice message. |
| `data.errorCode` | number | Gateway error code when a receipt failure occurs. |
| `data.errorText` | string | Gateway error message when a receipt failure occurs. |
| `data.messageId` | string | Message identifier for the SMS receipt. |
| `data.messageType` | string | Message type for the receipt, such as sms. |
| `data.statusCode` | number | Gateway status code for the receipt. |
| `data.statusText` | string | Gateway status message for the receipt. |
| `data.subaccountId` | number | Sub-account identifier that owns the SMS. |
| `data.timestamp` | number | Unix timestamp when the receipt was recorded. |
| `data.timestampSend` | number | Unix timestamp when the SMS was sent. |
| `httpCode` | number | HTTP code returned by ClickSend. |
| `responseCode` | string | ClickSend response code. |
| `responseMsg` | string | Outcome message for the receipt lookup. |

## Native endpoint

Through the native ClickSend SMS API, this operation is `GET /v3/sms/receipts/:message_id` (base URL `https://rest.clicksend.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sms-receipt.md) for the provider-specific parameters and requirements.

