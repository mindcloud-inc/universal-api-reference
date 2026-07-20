# OnlineCheckWriter: Update Payee Bank Account

Updates a specific bank account for a payee.

```
PUT https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/update-payee-bank-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnlineCheckWriter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/update-payee-bank-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "payeeBankAccountId": "string",
  "payeeId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/update-payee-bank-account', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "payeeBankAccountId": "string",
    "payeeId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `payeeBankAccountId` | string | yes | The payee bank account identifier. |
| `payeeId` | string | yes | The payee identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OnlineCheckWriter API returns.

## Native endpoint

Through the native OnlineCheckWriter API, this operation is `PUT /payees/:payeeId/bank-accounts/:payeeBankAccountId` (base URL `https://test.onlinecheckwriter.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-payee-bank-account.md) for the provider-specific parameters and requirements.

