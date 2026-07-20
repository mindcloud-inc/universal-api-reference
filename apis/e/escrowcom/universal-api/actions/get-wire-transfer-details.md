# Escrow.com: Get Wire Transfer Details

Retrieves wire transfer details from Escrow.com.

```
GET https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/get-wire-transfer-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Escrow.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/get-wire-transfer-details?connectionId=$CONNECTION_ID&transactionId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transactionId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/get-wire-transfer-details?${params}`, {
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
| `transactionId` | number | yes | The Escrow.com transaction ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "additionalInstructions": "string",
      "bankAddress": {},
      "bankName": "Ava Chen",
      "creditAccountName": "Ava Chen",
      "creditAccountNumber": "string",
      "routingNumber": "string",
      "structuredBankAddress": {},
      "structuredWireBenAddress": {},
      "swiftCode": "string",
      "wireBeneficiaryAddress": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `additionalInstructions` | string | Additional wire transfer instructions. |
| `bankAddress` | object | Receiving bank address. |
| `bankName` | string | Receiving bank name. |
| `creditAccountName` | string | Escrow.com receiving account name. |
| `creditAccountNumber` | string | Receiving account number. |
| `routingNumber` | string | Bank routing number when returned. |
| `structuredBankAddress` | object | Structured receiving bank address. |
| `structuredWireBenAddress` | object | Structured wire beneficiary address. |
| `swiftCode` | string | Bank SWIFT code when returned. |
| `wireBeneficiaryAddress` | string | Wire beneficiary address text. |

## Native endpoint

Through the native Escrow.com API, this operation is `GET /transaction/:transaction_id/payment_methods/wire_transfer` (base URL `https://api.escrow-sandbox.com/2017-09-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-wire-transfer-details.md) for the provider-specific parameters and requirements.

