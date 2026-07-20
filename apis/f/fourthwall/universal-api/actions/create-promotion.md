# Fourthwall: Create Promotion

Creates a new promotion in Fourthwall.

```
POST https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/create-promotion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fourthwall `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/create-promotion" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "MEMBERSHIPS_MULTI",
  "discount": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/create-promotion', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "MEMBERSHIPS_MULTI",
    "discount": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | list | yes | Promotion type. Supported values: SHOP_SINGLE, SHOP_MULTI, MEMBERSHIPS_SINGLE, MEMBERSHIPS_MULTI. One of: `MEMBERSHIPS_MULTI`, `MEMBERSHIPS_SINGLE`, `SHOP_MULTI`, `SHOP_SINGLE`. |
| `code` | string | no | Promotion code for single-code variants. |
| `codes[]` | array<string> | no | Array of promotion codes for multi-code variants. |
| `discount` | object | yes | Discount object. For shop promotions use either a fixed amount discount or percentage discount. For membership promotions use percentage discount. |
| `requirements` | object | no | Requirements object. For memberships, set newMembersOnly. For shop promotions, minimumOrderValue may be provided. |
| `subscriptionType` | list | no | Membership subscription type selector for membership promotion variants. One of: `ALL`, `ANNUAL`, `MONTHLY`. |
| `tiers` | object | no | Membership tiers selector object for membership promotion variants. |
| `appliesToProducts` | object | no | Selected products object for shop promotion variants. productIds is required if this object is provided. |
| `limits` | object | no | Promotion limits object for shop promotion variants. oneUsePerCustomer is required if this object is provided. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appliesTo": {
        "type": "string"
      },
      "code": "string",
      "discount": {
        "percentage": 1,
        "shippingOption": "string",
        "type": "string"
      },
      "id": "string",
      "limits": {
        "maximumUsesNumber": 1,
        "oneUsePerCustomer": true
      },
      "requirements": {
        "minimumOrderValue": 1
      },
      "status": "string",
      "type": "string",
      "usageCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appliesTo.type` | string | Which items or order scope the promotion applies to. |
| `code` | string | Promotion code shown to customers. |
| `discount.percentage` | number | Percentage discount amount when applicable. |
| `discount.shippingOption` | string | Shipping discount behavior. |
| `discount.type` | string | Discount type. |
| `id` | string | Fourthwall promotion ID. |
| `limits.maximumUsesNumber` | number | Maximum allowed uses when configured. |
| `limits.oneUsePerCustomer` | boolean | Whether each customer can use the promotion only once. |
| `requirements.minimumOrderValue` | number | Minimum order value required to apply the promotion. |
| `status` | string | Current promotion status. |
| `type` | string | Promotion type. |
| `usageCount` | number | How many times the promotion has been used. |

## Native endpoint

Through the native Fourthwall API, this operation is `POST /open-api/v1.0/promotions` (base URL `https://api.fourthwall.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-promotion.md) for the provider-specific parameters and requirements.

