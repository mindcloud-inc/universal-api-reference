# Easyship: Get Shipping Rule

Retrieves a shipping rule from Easyship.

```
GET https://connect.mindcloud.co/v1/universal/easyship/latest/actions/get-shipping-rule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easyship `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyship/latest/actions/get-shipping-rule?connectionId=$CONNECTION_ID&shippingRuleId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "shippingRuleId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyship/latest/actions/get-shipping-rule?${params}`, {
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
| `shippingRuleId` | string | yes | The Easyship shipping rule ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessible": true,
      "actions": [
        [
          {}
        ]
      ],
      "active": true,
      "checkoutRestrictive": true,
      "conditions": [
        [
          {}
        ]
      ],
      "createdAt": "string",
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "priority": 1,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessible` | boolean |  |
| `actions[]` | array<object> |  |
| `actions[].id` | string |  |
| `actions[].type` | string |  |
| `active` | boolean |  |
| `checkoutRestrictive` | boolean |  |
| `conditions[]` | array<object> |  |
| `conditions[].id` | string |  |
| `conditions[].type` | string |  |
| `createdAt` | string |  |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |
| `priority` | number |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Easyship API, this operation is `GET /shipping_rules/:shipping_rule_id` (base URL `https://public-api.easyship.com/2024-09`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shipping-rule.md) for the provider-specific parameters and requirements.

