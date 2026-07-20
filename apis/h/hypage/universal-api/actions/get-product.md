# Hy.page: Get Product



```
GET https://connect.mindcloud.co/v1/universal/hypage/latest/actions/get-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hy.page `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hypage/latest/actions/get-product?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hypage/latest/actions/get-product?${params}`, {
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
| `id` | string | yes | Product ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "description": "string",
      "id": "string",
      "isActive": true,
      "maxAttendees": 1,
      "meetingDuration": 1,
      "meetingLocation": "string",
      "meetingLocationType": "string",
      "meetingType": "string",
      "membershipDuration": 1,
      "price": 1,
      "pricingType": "string",
      "productSpecs": {},
      "recurringBilling": true,
      "skus": [
        {}
      ],
      "slug": "string",
      "title": "string",
      "trialDays": 1,
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `currency` | string |  |
| `description` | string |  |
| `id` | string |  |
| `isActive` | boolean |  |
| `maxAttendees` | number |  |
| `meetingDuration` | number |  |
| `meetingLocation` | string |  |
| `meetingLocationType` | string |  |
| `meetingType` | string |  |
| `membershipDuration` | number |  |
| `price` | number |  |
| `pricingType` | string |  |
| `productSpecs` | object |  |
| `recurringBilling` | boolean |  |
| `skus` | array<object> |  |
| `slug` | string |  |
| `title` | string |  |
| `trialDays` | number |  |
| `type` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Hy.page API, this operation is `GET /hyax-api/v1/products/:id` (base URL `https://platform.hyax.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product.md) for the provider-specific parameters and requirements.

