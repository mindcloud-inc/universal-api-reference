# Loqate: Batch Validate Bank Accounts

Validates multiple bank accounts with Loqate.

```
GET https://connect.mindcloud.co/v1/universal/loqate/latest/actions/batch-validate-bank-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loqate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loqate/latest/actions/batch-validate-bank-accounts?connectionId=$CONNECTION_ID&accountNumbers=string&sortCodes=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountNumbers": "string",
  "sortCodes": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loqate/latest/actions/batch-validate-bank-accounts?${params}`, {
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
| `accountNumbers` | string | yes | Comma-separated bank account numbers to validate. |
| `sortCodes` | string | yes | Comma-separated branch sort codes for the account numbers. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bank": "string",
      "bankBIC": "string",
      "branch": "string",
      "branchBIC": "string",
      "contactAddressLine1": "string",
      "contactAddressLine2": "string",
      "contactFax": "string",
      "contactPhone": "string",
      "contactPostcode": "string",
      "contactPostTown": "string",
      "correctedAccountNumber": "string",
      "correctedSortCode": "string",
      "iban": "string",
      "isCorrect": true,
      "isDirectDebitCapable": true,
      "originalAccountNumber": "string",
      "originalSortCode": "string",
      "statusInformation": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bank` | string |  |
| `bankBIC` | string |  |
| `branch` | string |  |
| `branchBIC` | string |  |
| `contactAddressLine1` | string |  |
| `contactAddressLine2` | string |  |
| `contactFax` | string |  |
| `contactPhone` | string |  |
| `contactPostcode` | string |  |
| `contactPostTown` | string |  |
| `correctedAccountNumber` | string |  |
| `correctedSortCode` | string |  |
| `iban` | string |  |
| `isCorrect` | boolean |  |
| `isDirectDebitCapable` | boolean |  |
| `originalAccountNumber` | string |  |
| `originalSortCode` | string |  |
| `statusInformation` | string |  |

## Native endpoint

Through the native Loqate API, this operation is `GET /BankAccountValidation/Batch/Validate/v1.00/json6.ws` (base URL `https://api.addressy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-validate-bank-accounts.md) for the provider-specific parameters and requirements.

