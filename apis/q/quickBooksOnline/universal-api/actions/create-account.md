# QuickBooks Online: Create Account



```
POST https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/create-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickBooks Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/create-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Office Supplies",
  "accountType": "Expense"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/create-account', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Office Supplies",
    "accountType": "Expense"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Account name. Example: `Office Supplies`. |
| `accountType` | string | yes | QuickBooks account type. Example: `Expense`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountSubType": "string",
      "accountType": "string",
      "active": true,
      "classification": "string",
      "currentBalance": 1,
      "fullyQualifiedName": "Ava Chen",
      "id": "string",
      "metaData": {},
      "name": "Ava Chen",
      "syncToken": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountSubType` | string |  |
| `accountType` | string |  |
| `active` | boolean |  |
| `classification` | string |  |
| `currentBalance` | number |  |
| `fullyQualifiedName` | string |  |
| `id` | string |  |
| `metaData` | object |  |
| `name` | string |  |
| `syncToken` | string |  |

## Native endpoint

Through the native QuickBooks Online API, this operation is `POST /account` (base URL `https://:quickbooksEnvironment/v3/company/:realmId`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-account.md) for the provider-specific parameters and requirements.

