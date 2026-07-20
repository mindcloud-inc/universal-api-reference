# QuickBooks Online: List Items



```
GET https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/list-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickBooks Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/list-items?connectionId=$CONNECTION_ID&query=select%20*%20from%20Item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "select * from Item"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/list-items?${params}`, {
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
| `query` | string | yes | Fixed query used to list items. Default: `select * from Item`. |

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

Through the native QuickBooks Online API, this operation is `GET /query` (base URL `https://:quickbooksEnvironment/v3/company/:realmId`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-items.md) for the provider-specific parameters and requirements.

