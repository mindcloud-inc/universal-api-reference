# Kiwili: Get Bank Account Details

Retrieves details for a bank account in Kiwili.

```
GET https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-bank-account-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kiwili `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-bank-account-details?connectionId=$CONNECTION_ID&bank_account_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bank_account_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-bank-account-details?${params}`, {
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
| `bank_account_id` | string | yes | The Kiwili bank account ID. Use the string 0 for the default record when needed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "AccountNumber": "string",
      "BankNumber": "string",
      "BranchNumber": "string",
      "Currency": "string",
      "Id": 1,
      "IsActive": true,
      "Name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AccountNumber` | string |  |
| `BankNumber` | string |  |
| `BranchNumber` | string |  |
| `Currency` | string |  |
| `Id` | number |  |
| `IsActive` | boolean |  |
| `Name` | string |  |

## Native endpoint

Through the native Kiwili API, this operation is `GET /bankaccount/:bank_account_id` (base URL `https://mindcloud.kiwili.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bank-account-details.md) for the provider-specific parameters and requirements.

