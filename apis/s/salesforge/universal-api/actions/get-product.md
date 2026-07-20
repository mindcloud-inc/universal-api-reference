# Salesforge: Get Product

Retrieves a product from Salesforge.

```
GET https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/get-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesforge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/get-product?connectionId=$CONNECTION_ID&workspaceId=wks_lxxtq91neaixc8yaiqp7w&productId=prod_zg3hw6s94gej81i28tw91" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "wks_lxxtq91neaixc8yaiqp7w",
  "productId": "prod_zg3hw6s94gej81i28tw91"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/get-product?${params}`, {
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
| `workspaceId` | string | yes | Example: `wks_lxxtq91neaixc8yaiqp7w`. |
| `productId` | string | yes | Example: `prod_zg3hw6s94gej81i28tw91`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "internalName": "Ava Chen",
      "translations": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `internalName` | string |  |
| `translations` | array<object> |  |

## Native endpoint

Through the native Salesforge API, this operation is `GET /public/v2/workspaces/:workspaceID/products/:productID` (base URL `https://api.salesforge.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product.md) for the provider-specific parameters and requirements.

