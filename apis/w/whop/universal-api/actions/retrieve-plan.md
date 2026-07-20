# Whop: Retrieve Plan

Retrieves plan details from the Whop platform.

```
GET https://connect.mindcloud.co/v1/universal/whop/latest/actions/retrieve-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Whop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whop/latest/actions/retrieve-plan?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whop/latest/actions/retrieve-plan?${params}`, {
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
| `id` | string | yes | The unique identifier of the plan. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "collectTax": true,
      "company": {
        "id": "string",
        "title": "string"
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "customFields": [
        "string"
      ],
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
      "taxType": "string",
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
| `collectTax` | boolean |  |
| `company` | object |  |
| `company.id` | string |  |
| `company.title` | string |  |
| `createdAt` | date |  |
| `currency` | string |  |
| `customFields` | array |  |
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
| `taxType` | string |  |
| `unlimitedStock` | boolean |  |
| `updatedAt` | date |  |
| `visibility` | string |  |

## Native endpoint

Through the native Whop API, this operation is `GET /api/v1/plans/:id` (base URL `https://api.whop.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-plan.md) for the provider-specific parameters and requirements.

