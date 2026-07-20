# Loqate: Validate Bank Account

Validates a bank account with Loqate.

```
GET https://connect.mindcloud.co/v1/universal/loqate/latest/actions/validate-bank-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loqate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loqate/latest/actions/validate-bank-account?connectionId=$CONNECTION_ID&accountNumber=string&sortCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountNumber": "string",
  "sortCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loqate/latest/actions/validate-bank-account?${params}`, {
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
| `accountNumber` | string | yes | The bank account number to validate. |
| `sortCode` | string | yes | The branch sort code for the account number. |

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
      "cHAPSSupported": true,
      "contactAddressLine1": "string",
      "contactAddressLine2": "string",
      "contactFax": "string",
      "contactPhone": "string",
      "contactPostcode": "string",
      "contactPostTown": "string",
      "correctedAccountNumber": "string",
      "correctedSortCode": "string",
      "fasterPaymentsSupported": true,
      "iban": "string",
      "isCorrect": true,
      "isDirectDebitCapable": true,
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
| `cHAPSSupported` | boolean |  |
| `contactAddressLine1` | string |  |
| `contactAddressLine2` | string |  |
| `contactFax` | string |  |
| `contactPhone` | string |  |
| `contactPostcode` | string |  |
| `contactPostTown` | string |  |
| `correctedAccountNumber` | string |  |
| `correctedSortCode` | string |  |
| `fasterPaymentsSupported` | boolean |  |
| `iban` | string |  |
| `isCorrect` | boolean |  |
| `isDirectDebitCapable` | boolean |  |
| `statusInformation` | string |  |

## Native endpoint

Through the native Loqate API, this operation is `GET /BankAccountValidation/Interactive/Validate/v2.00/json6.ws` (base URL `https://api.addressy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-bank-account.md) for the provider-specific parameters and requirements.

