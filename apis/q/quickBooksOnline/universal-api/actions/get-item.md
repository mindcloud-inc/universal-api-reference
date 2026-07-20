# QuickBooks Online: Get Item



```
GET https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/get-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickBooks Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/get-item?connectionId=$CONNECTION_ID&itemId=%5B%20%2225%22%2C%22121%22%2C%2238%22%2C%22114%22%2C%2244%22%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "itemId": "[ \"25\",\"121\",\"38\",\"114\",\"44\"]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/get-item?${params}`, {
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
| `itemId` | string | yes | QuickBooks Item Id. Default: `[ \"25\",\"121\",\"38\",\"114\",\"44\"]`. |
| `query` | string | no | Default: `select * from Item where Id in (ItemId) order by Metadata.LastUpdatedTime DESC`. |

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

Through the native QuickBooks Online API, this operation is `GET /item/:itemId` (base URL `https://:quickbooksEnvironment/v3/company/:realmId`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-item.md) for the provider-specific parameters and requirements.

