# Framework360: List Order



```
GET https://connect.mindcloud.co/v1/universal/framework360/latest/actions/orders-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Framework360 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/framework360/latest/actions/orders-list?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/framework360/latest/actions/orders-list?${params}`, {
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
| `seller` | string | no | Seller identifier. |
| `orderId` | number | no | Specific order ID to filter by. |
| `customerId` | number | no | Customer ID to filter orders by. |
| `page` | number | no | Results page number. |
| `dateRange` | string | no | Date range filter. |
| `sortOrder` | string | no | Sort order direction. |
| `limit` | number | no | Maximum number of items per page. |
| `amount` | number | no | Order amount filter. |
| `query` | string | no | Free-text search term. |
| `statuses[]` | array<string> | no | Order statuses to filter by. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Framework360 API returns.

## Native endpoint

Through the native Framework360 API, this operation is `GET orders/list` (base URL `https://mindcloudstage0.framework360.site/m/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/orders-list.md) for the provider-specific parameters and requirements.

