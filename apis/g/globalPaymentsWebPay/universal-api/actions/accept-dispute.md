# Global Payments WebPay: Accept Dispute

Updates a dispute by accepting it in Global Payments WebPay.

```
PUT https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/accept-dispute
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Global Payments WebPay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/accept-dispute" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/accept-dispute', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Global Payments dispute ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": {
        "id": "string"
      },
      "amount": "string",
      "currency": "string",
      "id": "string",
      "reason_code": "string",
      "result": "string",
      "stage": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action.id` | string |  |
| `amount` | string |  |
| `currency` | string |  |
| `id` | string |  |
| `reason_code` | string |  |
| `result` | string |  |
| `stage` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Global Payments WebPay API, this operation is `POST /disputes/{id}/acceptance` (base URL `https://apis.globalpay.com/ucp`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/accept-dispute.md) for the provider-specific parameters and requirements.

