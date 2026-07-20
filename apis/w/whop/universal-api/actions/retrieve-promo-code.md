# Whop: Retrieve Promo Code

Retrieves promo code details from the Whop platform.

```
GET https://connect.mindcloud.co/v1/universal/whop/latest/actions/retrieve-promo-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Whop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whop/latest/actions/retrieve-promo-code?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whop/latest/actions/retrieve-promo-code?${params}`, {
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
| `id` | string | yes | The unique identifier of the promo code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amountOff": 1,
      "churnedUsersOnly": true,
      "code": "string",
      "company": {
        "id": "string",
        "title": "string"
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "duration": "string",
      "existingMembershipsOnly": true,
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "newUsersOnly": true,
      "onePerCustomer": true,
      "product": {
        "id": "string",
        "title": "string"
      },
      "promoDurationMonths": 1,
      "promoType": "string",
      "status": "string",
      "stock": 1,
      "unlimitedStock": true,
      "uses": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amountOff` | number |  |
| `churnedUsersOnly` | boolean |  |
| `code` | string |  |
| `company` | object |  |
| `company.id` | string |  |
| `company.title` | string |  |
| `createdAt` | date |  |
| `currency` | string |  |
| `duration` | string |  |
| `existingMembershipsOnly` | boolean |  |
| `expiresAt` | date |  |
| `id` | string |  |
| `newUsersOnly` | boolean |  |
| `onePerCustomer` | boolean |  |
| `product` | object |  |
| `product.id` | string |  |
| `product.title` | string |  |
| `promoDurationMonths` | number |  |
| `promoType` | string |  |
| `status` | string |  |
| `stock` | number |  |
| `unlimitedStock` | boolean |  |
| `uses` | number |  |

## Native endpoint

Through the native Whop API, this operation is `GET /api/v1/promo_codes/:id` (base URL `https://api.whop.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-promo-code.md) for the provider-specific parameters and requirements.

