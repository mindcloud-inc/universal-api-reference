# Bridge: Get Payout

Retrieves a payout from Bridge.

```
GET https://connect.mindcloud.co/v1/universal/bridge/latest/actions/get-payout
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridge/latest/actions/get-payout?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridge/latest/actions/get-payout?${params}`, {
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
| `id` | string | yes |  |

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

Through the native Bridge API, this operation is `GET /payment/payment-account/payouts/:id` (base URL `https://api.bridgeapi.io/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-payout.md) for the provider-specific parameters and requirements.

