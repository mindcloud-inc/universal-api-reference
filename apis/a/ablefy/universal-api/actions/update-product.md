# Ablefy: Update Product

Updates an existing product in Ablefy.

```
PUT https://connect.mindcloud.co/v1/universal/ablefy/latest/actions/update-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ablefy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ablefy/latest/actions/update-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ablefy/latest/actions/update-product', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Product ID. |
| `name` | string | yes | Product name. |
| `successUrl` | string | no |  |
| `cancelUrl` | string | no |  |
| `errorUrl` | string | no |  |
| `webhookEndpointIds[]` | array<string> | no |  |
| `webhookUrl` | string | no |  |
| `pageHeader` | string | no |  |
| `pageFooter` | string | no |  |
| `free` | boolean | no |  |
| `active` | boolean | no |  |
| `private` | boolean | no |  |
| `performancePeriod` | boolean | no |  |
| `performancePeriodType` | string | no |  |
| `performancePeriodText` | string | no |  |
| `form` | string | no |  |
| `webhookEndpointForm` | string | no |  |
| `forward` | object | no |  |
| `teamMembers[]` | array<object> | no |  |
| `pricesAttributes[]` | array<object> | no |  |
| `successEmail` | object | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ablefy API returns.

## Native endpoint

Through the native Ablefy API, this operation is `PUT /api/products/:id` (base URL `https://api.myablefy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-product.md) for the provider-specific parameters and requirements.

