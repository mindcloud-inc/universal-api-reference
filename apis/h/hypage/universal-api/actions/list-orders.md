# Hy.page: List Orders



```
GET https://connect.mindcloud.co/v1/universal/hypage/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hy.page `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hypage/latest/actions/list-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hypage/latest/actions/list-orders?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "fulfillmentStatus": "string",
      "id": "string",
      "isTest": true,
      "itemCount": 1,
      "itemsData": {},
      "notes": "string",
      "orderNumber": "string",
      "paymentDate": "2026-05-07T12:00:00.000Z",
      "paymentPlatform": "string",
      "paymentStatus": "string",
      "people": {},
      "peopleId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | string |  |
| `createdAt` | date |  |
| `currency` | string |  |
| `fulfillmentStatus` | string |  |
| `id` | string |  |
| `isTest` | boolean |  |
| `itemCount` | number |  |
| `itemsData` | object |  |
| `notes` | string |  |
| `orderNumber` | string |  |
| `paymentDate` | date |  |
| `paymentPlatform` | string |  |
| `paymentStatus` | string |  |
| `people` | object |  |
| `peopleId` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Hy.page API, this operation is `GET /hyax-api/v1/orders` (base URL `https://platform.hyax.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

