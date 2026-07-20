# QuickBooks Online: Create Vendor



```
POST https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/create-vendor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickBooks Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/create-vendor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "displayName": "Acme Supplies"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/create-vendor', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "displayName": "Acme Supplies"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `displayName` | string | yes | Vendor display name. Example: `Acme Supplies`. |

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
| `id` | string |  |
| `metaData` | object |  |
| `primaryEmailAddr` | object |  |
| `syncToken` | string |  |

## Native endpoint

Through the native QuickBooks Online API, this operation is `POST /vendor` (base URL `https://:quickbooksEnvironment/v3/company/:realmId`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-vendor.md) for the provider-specific parameters and requirements.

