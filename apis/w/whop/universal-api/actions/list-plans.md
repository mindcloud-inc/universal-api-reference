# Whop: List Plans

Retrieves subscription plans from Whop for a company.

```
GET https://connect.mindcloud.co/v1/universal/whop/latest/actions/list-plans
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Whop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whop/latest/actions/list-plans?connectionId=$CONNECTION_ID&companyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whop/latest/actions/list-plans?${params}`, {
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
| `companyId` | string | yes | The unique identifier of the company to list plans for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": {
        "id": "string",
        "title": "string"
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "id": "string",
      "initialPrice": 1,
      "internalNotes": "string",
      "memberCount": 1,
      "planType": "string",
      "product": {
        "id": "string",
        "title": "string"
      },
      "purchaseUrl": "https://example.com",
      "releaseMethod": "string",
      "renewalPrice": 1,
      "stock": 1,
      "unlimitedStock": true,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | object |  |
| `company.id` | string |  |
| `company.title` | string |  |
| `createdAt` | date |  |
| `currency` | string |  |
| `id` | string |  |
| `initialPrice` | number |  |
| `internalNotes` | string |  |
| `memberCount` | number |  |
| `planType` | string |  |
| `product` | object |  |
| `product.id` | string |  |
| `product.title` | string |  |
| `purchaseUrl` | string |  |
| `releaseMethod` | string |  |
| `renewalPrice` | number |  |
| `stock` | number |  |
| `unlimitedStock` | boolean |  |
| `updatedAt` | date |  |
| `visibility` | string |  |

## Native endpoint

Through the native Whop API, this operation is `GET /api/v1/plans` (base URL `https://api.whop.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-plans.md) for the provider-specific parameters and requirements.

