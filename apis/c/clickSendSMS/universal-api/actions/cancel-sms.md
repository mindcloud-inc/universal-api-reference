# ClickSend SMS: Cancel SMS

Cancels an SMS message in ClickSend SMS.

```
PUT https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/cancel-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickSend SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/cancel-sms" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "message_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/cancel-sms', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "message_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `message_id` | string | yes | Outbound message identifier to cancel. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "httpCode": "string",
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
| `httpCode` | string | HTTP code returned by ClickSend for the cancel request. |
| `responseCode` | string | ClickSend response code for the cancel request. |
| `responseMsg` | string | Outcome message for the cancel request. |

## Native endpoint

Through the native ClickSend SMS API, this operation is `PUT /v3/sms/:message_id/cancel` (base URL `https://rest.clicksend.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-sms.md) for the provider-specific parameters and requirements.

