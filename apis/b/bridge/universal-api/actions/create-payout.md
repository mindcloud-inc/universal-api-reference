# Bridge: Create Payout

Creates a payout in Bridge.

```
POST https://connect.mindcloud.co/v1/universal/bridge/latest/actions/create-payout
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bridge/latest/actions/create-payout" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "beneficiaryId": "string",
  "amount": 1,
  "label": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bridge/latest/actions/create-payout', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "beneficiaryId": "string",
    "amount": 1,
    "label": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `beneficiaryId` | string | yes | The id of the payout beneficiary to which you wish to transfer money |
| `amount` | number | yes | The amount you wish to transfer, positive and up to 2 decimals |
| `label` | string | yes | This label that will be displayed on your bank account (140 characters max.) |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientReference` | string | no | An optional reference to link this payout request to your system (100 characters max.) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "beneficiary": {
        "bankName": "Ava Chen",
        "bic": "string",
        "companyName": "Ava Chen",
        "iban": "string",
        "id": "string"
      },
      "clientReference": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "id": "string",
      "label": "string",
      "status": "string",
      "type": "string",
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
| `beneficiary` | object |  |
| `beneficiary.bankName` | string |  |
| `beneficiary.bic` | string |  |
| `beneficiary.companyName` | string |  |
| `beneficiary.iban` | string |  |
| `beneficiary.id` | string |  |
| `clientReference` | string | Your internal reference for reconciliation |
| `createdAt` | date |  |
| `currency` | string |  |
| `id` | string |  |
| `label` | string | Label of the payout |
| `status` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Bridge API, this operation is `POST /payment/payment-account/payouts` (base URL `https://api.bridgeapi.io/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-payout.md) for the provider-specific parameters and requirements.

