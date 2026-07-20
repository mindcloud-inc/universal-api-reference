# Column: Create Counterparty



```
POST https://connect.mindcloud.co/v1/universal/column/latest/actions/create-counterparty
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Column `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/column/latest/actions/create-counterparty" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "routingNumber": "string",
  "accountNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/column/latest/actions/create-counterparty', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "routingNumber": "string",
    "accountNumber": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `routingNumber` | string | yes | The routing number of the bank. |
| `accountNumber` | string | yes | The account number of the bank account. |
| `accountType` | list | no | The type of the account number. Can be checking or savings. One of: `0`, `1`. |
| `routingNumberType` | list | no | The type of the routing number. Can be aba or bic. One of: `0`, `1`. |
| `description` | string | no | Description of the counterparty visible only in your platform. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountNumber": "string",
      "accountType": "string",
      "address": {},
      "createdAt": "string",
      "description": "string",
      "email": "ava@example.com",
      "id": "string",
      "isColumnAccount": true,
      "legalId": "string",
      "legalType": "string",
      "localAccountNumber": "string",
      "localBankCode": "string",
      "localBankCountryCode": "string",
      "localBankName": "Ava Chen",
      "name": "Ava Chen",
      "phone": "string",
      "routingNumber": "string",
      "routingNumberType": "string",
      "updatedAt": "string",
      "wire": {},
      "wireDrawdownAllowed": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountNumber` | string |  |
| `accountType` | string |  |
| `address` | object |  |
| `createdAt` | string |  |
| `description` | string |  |
| `email` | string |  |
| `id` | string |  |
| `isColumnAccount` | boolean |  |
| `legalId` | string |  |
| `legalType` | string |  |
| `localAccountNumber` | string |  |
| `localBankCode` | string |  |
| `localBankCountryCode` | string |  |
| `localBankName` | string |  |
| `name` | string |  |
| `phone` | string |  |
| `routingNumber` | string |  |
| `routingNumberType` | string |  |
| `updatedAt` | string |  |
| `wire` | object |  |
| `wireDrawdownAllowed` | boolean |  |

## Native endpoint

Through the native Column API, this operation is `POST /counterparties` (base URL `https://api.column.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-counterparty.md) for the provider-specific parameters and requirements.

