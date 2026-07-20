# Digistore24: Update Product Group

Updates an existing product group in Digistore24.

```
PUT https://connect.mindcloud.co/v1/universal/digistore24/latest/actions/update-product-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digistore24 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/digistore24/latest/actions/update-product-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productGroupId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/digistore24/latest/actions/update-product-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productGroupId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productGroupId` | number | yes | Product group ID |
| `name` | string | no | Product group name |
| `position` | number | no | Display order |
| `isShownAsTab` | boolean | no | Display group as tab |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Digistore24 API returns.

## Native endpoint

Through the native Digistore24 API, this operation is `PUT /updateProductGroup` (base URL `https://www.digistore24.com/api/call`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-product-group.md) for the provider-specific parameters and requirements.

