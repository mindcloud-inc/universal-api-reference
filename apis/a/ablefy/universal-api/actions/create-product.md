# Ablefy: Create Product

Creates a new product in Ablefy.

```
POST https://connect.mindcloud.co/v1/universal/ablefy/latest/actions/create-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ablefy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ablefy/latest/actions/create-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ablefy/latest/actions/create-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `forward.campaignId` | string | no |  |
| `forward.coupon` | string | no |  |
| `forward.email` | string | no |  |
| `forward.firstName` | string | no |  |
| `forward.lastName` | string | no |  |
| `name` | string | yes | Product name. |
| `pricesAttributes[].id` | number | no |  |
| `pricesAttributes[].position` | number | no |  |
| `pricesAttributes[].pricingPlanId` | number | no |  |
| `successEmail.bodyDe` | string | no |  |
| `successEmail.bodyEn` | string | no |  |
| `successEmail.subjectDe` | string | no |  |
| `successEmail.subjectEn` | string | no |  |
| `teamMembers[].commission` | number | no |  |
| `teamMembers[].id` | number | no |  |
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
| `performancePeriodType` | list<string> | no | One of: `custom_text`, `purchase_date`, `relative_date`. |
| `performancePeriodText` | string | no |  |
| `form` | list<string> | no | One of: `course`, `download`, `event`, `service`. |
| `webhookEndpointForm` | list<string> | no | One of: `all_webhook_endpoints`, `no_webhook_endpoints`, `selected_webhook_endpoints`. |
| `forward` | object | no |  |
| `teamMembers[]` | array<object> | no |  |
| `pricesAttributes[]` | array<object> | no |  |
| `successEmail` | object | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ablefy API returns.

## Native endpoint

Through the native Ablefy API, this operation is `POST /api/products` (base URL `https://api.myablefy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product.md) for the provider-specific parameters and requirements.

