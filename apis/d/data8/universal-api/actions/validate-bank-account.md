# Data8: Validate Bank Account

Validates a bank account with Data8.

```
GET https://connect.mindcloud.co/v1/universal/data8/latest/actions/validate-bank-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Data8 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/data8/latest/actions/validate-bank-account?connectionId=$CONNECTION_ID&sortCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sortCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/data8/latest/actions/validate-bank-account?${params}`, {
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
| `sortCode` | string | yes | The sort code to validate. |
| `bankAccountNumber` | string | no | The optional account number to validate. |
| `options` | object | no | Optional settings that control bank validation behavior. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "AccountNumber": "string",
      "Address": {
        "RawAddress": {
          "Postcode": "string"
        }
      },
      "BICCode": "string",
      "BranchName": "Ava Chen",
      "FullBankName": "Ava Chen",
      "SortCode": "string",
      "Status": {
        "CreditsRemaining": 1,
        "ErrorMessage": "string",
        "Success": true
      },
      "Valid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AccountNumber` | string |  |
| `Address.RawAddress.Postcode` | string |  |
| `BICCode` | string |  |
| `BranchName` | string |  |
| `FullBankName` | string |  |
| `SortCode` | string |  |
| `Status.CreditsRemaining` | number |  |
| `Status.ErrorMessage` | string |  |
| `Status.Success` | boolean |  |
| `Valid` | string |  |

## Native endpoint

Through the native Data8 API, this operation is `POST /BankAccountValidation/IsValid.json` (base URL `https://webservices.data-8.co.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-bank-account.md) for the provider-specific parameters and requirements.

