# Megaventory: Update Product Supplier

Updates a product supplier link in Megaventory using a record action.

```
PUT https://connect.mindcloud.co/v1/universal/megaventory/latest/actions/update-product-supplier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Megaventory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/megaventory/latest/actions/update-product-supplier" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mvProductSupplierUpdate": {},
  "mvRecordAction": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/megaventory/latest/actions/update-product-supplier', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mvProductSupplierUpdate": {},
    "mvRecordAction": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mvProductSupplierUpdate` | object | yes | Product and supplier relationship payload to insert, update, or delete. |
| `mvRecordAction` | string | yes | Megaventory record action such as Insert, Update, or Delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "mvProductSupplier": {},
      "ResponseStatus": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `mvProductSupplier` | object |  |
| `ResponseStatus` | object |  |

## Native endpoint

Through the native Megaventory API, this operation is `POST /json/reply/ProductSupplierUpdate` (base URL `https://api.megaventory.com/v2017a`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-product-supplier.md) for the provider-specific parameters and requirements.

