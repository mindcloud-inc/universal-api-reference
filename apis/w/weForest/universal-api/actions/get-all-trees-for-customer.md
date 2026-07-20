# WeForest: Get all trees for customer

Retrieves all trees for a customer in WeForest.

```
GET https://connect.mindcloud.co/v1/universal/weForest/latest/actions/get-all-trees-for-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WeForest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weForest/latest/actions/get-all-trees-for-customer?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weForest/latest/actions/get-all-trees-for-customer?${params}`, {
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
| `id` | number | yes | Customer identifier from WeForest. |
| `count` | boolean | no | Fetch the total count of all order quantities. |
| `startDate` | string | no | Start of date range for order requests in YYYY-MM-DD format. |
| `endDate` | string | no | End of date range for order requests in YYYY-MM-DD format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customerId": 1,
      "endUser": {},
      "id": 1,
      "items": [
        {}
      ],
      "paid": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `customerId` | number |  |
| `endUser` | object |  |
| `id` | number |  |
| `items` | array<object> |  |
| `paid` | boolean |  |

## Native endpoint

Through the native WeForest API, this operation is `GET /customers/:id/trees` (base URL `https://api.weforest.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-trees-for-customer.md) for the provider-specific parameters and requirements.

