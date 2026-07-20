# Fourthwall: Get Promotion

Retrieves a promotion from Fourthwall by ID.

```
GET https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/get-promotion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fourthwall `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/get-promotion?connectionId=$CONNECTION_ID&promotionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "promotionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/get-promotion?${params}`, {
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
| `promotionId` | string | yes | The promotion ID. |

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

Through the native Fourthwall API, this operation is `GET /open-api/v1.0/promotions/:promotionId` (base URL `https://api.fourthwall.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-promotion.md) for the provider-specific parameters and requirements.

