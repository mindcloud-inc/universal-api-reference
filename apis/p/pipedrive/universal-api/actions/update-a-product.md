# Pipedrive: Update a Product

Updates an existing product in Pipedrive.

```
PUT https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/update-a-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/update-a-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/update-a-product', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productId` | number | yes |  |
| `name` | string | no |  |
| `code` | string | no |  |
| `description` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pipedrive API returns.

## Native endpoint

Through the native Pipedrive API, this operation is `PATCH v2/products/:productId` (base URL `{{credentials.accessTokenRequest.api_domain}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-a-product.md) for the provider-specific parameters and requirements.

