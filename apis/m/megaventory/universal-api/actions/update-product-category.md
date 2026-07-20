# Megaventory: Update Product Category

Updates a product category in Megaventory using a record action.

```
PUT https://connect.mindcloud.co/v1/universal/megaventory/latest/actions/update-product-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Megaventory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/megaventory/latest/actions/update-product-category" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mvProductCategory": {},
  "mvRecordAction": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/megaventory/latest/actions/update-product-category', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mvProductCategory": {},
    "mvRecordAction": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mvProductCategory` | object | yes | Product category payload to insert, update, or delete. |
| `mvRecordAction` | string | yes | Megaventory record action such as Insert, Update, or Delete. |
| `mvInsertUpdateDeleteSourceApplication` | string | no | Source application label Megaventory should store for the change. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entityID": 1,
      "mvProductCategory": {},
      "ResponseStatus": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entityID` | number |  |
| `mvProductCategory` | object |  |
| `ResponseStatus` | object |  |

## Native endpoint

Through the native Megaventory API, this operation is `POST /json/reply/ProductCategoryUpdate` (base URL `https://api.megaventory.com/v2017a`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-product-category.md) for the provider-specific parameters and requirements.

