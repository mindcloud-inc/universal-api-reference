# Whop: List Promo Codes

Retrieves promo codes from Whop for a company.

```
GET https://connect.mindcloud.co/v1/universal/whop/latest/actions/list-promo-codes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Whop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whop/latest/actions/list-promo-codes?connectionId=$CONNECTION_ID&companyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whop/latest/actions/list-promo-codes?${params}`, {
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
| `companyId` | string | yes | The unique identifier of the company to list promo codes for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amountOff": 1,
      "churnedUsersOnly": true,
      "code": "string",
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

Through the native Whop API, this operation is `GET /api/v1/promo_codes` (base URL `https://api.whop.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-promo-codes.md) for the provider-specific parameters and requirements.

