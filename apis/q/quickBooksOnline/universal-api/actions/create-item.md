# QuickBooks Online: Create Item



```
POST https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/create-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickBooks Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/create-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Consulting Service",
  "type": "Service",
  "incomeAccountRef.value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/create-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Consulting Service",
    "type": "Service",
    "incomeAccountRef.value": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Item name. Example: `Consulting Service`. |
| `type` | string | yes | QuickBooks item type. Example: `Service`. |
| `incomeAccountRef.value` | string | yes | Income account ID required when creating a service item in QuickBooks. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "expenseAccountRef": {},
      "fullyQualifiedName": "Ava Chen",
      "id": "string",
      "incomeAccountRef": {},
      "metaData": {},
      "name": "Ava Chen",
      "qtyOnHand": 1,
      "syncToken": "string",
      "type": "string",
      "unitPrice": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `expenseAccountRef` | object |  |
| `fullyQualifiedName` | string |  |
| `id` | string |  |
| `incomeAccountRef` | object |  |
| `metaData` | object |  |
| `name` | string |  |
| `qtyOnHand` | number |  |
| `syncToken` | string |  |
| `type` | string |  |
| `unitPrice` | number |  |

## Native endpoint

Through the native QuickBooks Online API, this operation is `POST /item` (base URL `https://:quickbooksEnvironment/v3/company/:realmId`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-item.md) for the provider-specific parameters and requirements.

