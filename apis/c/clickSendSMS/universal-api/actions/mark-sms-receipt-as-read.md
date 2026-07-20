# ClickSend SMS: Mark SMS Receipt As Read

Marks SMS receipts as read in ClickSend SMS.

```
PUT https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/mark-sms-receipt-as-read
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickSend SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/mark-sms-receipt-as-read" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dateBefore": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/mark-sms-receipt-as-read', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dateBefore": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dateBefore` | string | yes | Mark receipts as read before this timestamp/date. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
| `httpCode` | number |  |
| `responseCode` | string |  |
| `responseMsg` | string |  |

## Native endpoint

Through the native ClickSend SMS API, this operation is `PUT /v3/sms/receipts-read` (base URL `https://rest.clicksend.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mark-sms-receipt-as-read.md) for the provider-specific parameters and requirements.

