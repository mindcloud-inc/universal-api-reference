# Simla.com: List Order Methods

Retrieves order method records from Simla.com.

```
GET https://connect.mindcloud.co/v1/universal/simlacom/latest/actions/list-order-methods
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simla.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simlacom/latest/actions/list-order-methods?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simlacom/latest/actions/list-order-methods?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Simla.com API returns.

## Native endpoint

Through the native Simla.com API, this operation is `GET /api/v5/reference/order-methods` (base URL `https://apps2.simla.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-order-methods.md) for the provider-specific parameters and requirements.

