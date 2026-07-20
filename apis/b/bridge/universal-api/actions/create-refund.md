# Bridge: Create Refund

Creates a refund in Bridge.

```
POST https://connect.mindcloud.co/v1/universal/bridge/latest/actions/create-refund
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bridge/latest/actions/create-refund" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "paymentAccountTransactionId": "string",
  "amount": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bridge/latest/actions/create-refund', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "paymentAccountTransactionId": "string",
    "amount": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `paymentAccountTransactionId` | string | yes | The id of the payment account transaction you want to refund |
| `amount` | number | yes | The amount you wish to refund (positive and up to 2 decimals). You can partially refund the payment transaction. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientReference` | string | no | An optional reference to link this refund request to your system (100 characters max.) |
| `description` | string | no | This description is only for an internal purpose and will allow to have information on the Dashboard (140 characters max.) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "clientReference": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "description": "string",
      "id": "string",
      "paymentAccountTransactionId": "string",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `clientReference` | string | Your internal reference for reconciliation |
| `createdAt` | date |  |
| `currency` | string |  |
| `description` | string | Your internal description |
| `id` | string |  |
| `paymentAccountTransactionId` | string |  |
| `status` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Bridge API, this operation is `POST /payment/payment-account/refunds` (base URL `https://api.bridgeapi.io/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-refund.md) for the provider-specific parameters and requirements.

