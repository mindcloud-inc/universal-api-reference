# QuickBooks Online: Update Customer



```
PUT https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickBooks Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "syncToken": "0",
  "displayName": "Acme Dental"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/update-customer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "syncToken": "0",
    "displayName": "Acme Dental"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Customer Id to update. |
| `syncToken` | string | yes | Current QuickBooks SyncToken for optimistic locking. Example: `0`. |
| `displayName` | string | yes | Updated customer display name. Example: `Acme Dental`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "balance": 1,
      "companyName": "Ava Chen",
      "currencyRef": {},
      "displayName": "Ava Chen",
      "fullyQualifiedName": "Ava Chen",
      "id": "string",
      "metaData": {},
      "primaryEmailAddr": {},
      "syncToken": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `balance` | number |  |
| `companyName` | string |  |
| `currencyRef` | object |  |
| `displayName` | string |  |
| `fullyQualifiedName` | string |  |
| `id` | string |  |
| `metaData` | object |  |
| `primaryEmailAddr` | object |  |
| `syncToken` | string |  |

## Native endpoint

Through the native QuickBooks Online API, this operation is `POST /customer` (base URL `https://:quickbooksEnvironment/v3/company/:realmId`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer.md) for the provider-specific parameters and requirements.

