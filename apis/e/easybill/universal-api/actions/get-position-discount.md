# easybill: Get Position Discount

Retrieves a position discount from easybill by ID.

```
GET https://connect.mindcloud.co/v1/universal/easybill/latest/actions/get-position-discount
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a easybill `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easybill/latest/actions/get-position-discount?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easybill/latest/actions/get-position-discount?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native easybill API returns.

## Native endpoint

Through the native easybill API, this operation is `GET /discounts/position/{id}` (base URL `https://api.easybill.de/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-position-discount.md) for the provider-specific parameters and requirements.

