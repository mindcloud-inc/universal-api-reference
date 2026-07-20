# remberg: List Work Orders

Retrieves work orders from remberg.

```
GET https://connect.mindcloud.co/v1/universal/remberg/latest/actions/list-work-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a remberg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/remberg/latest/actions/list-work-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/remberg/latest/actions/list-work-orders?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native remberg API returns.

## Native endpoint

Through the native remberg API, this operation is `GET /v2/work-orders` (base URL `https://api.remberg.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-work-orders.md) for the provider-specific parameters and requirements.

