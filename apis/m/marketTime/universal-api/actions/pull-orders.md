# MarketTime: Pull Orders



```
GET https://connect.mindcloud.co/v1/universal/marketTime/latest/actions/pull-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MarketTime `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/marketTime/latest/actions/pull-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/marketTime/latest/actions/pull-orders?${params}`, {
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
| `filters[]` | array | no |  |
| `filters[].field` | list | no |  |
| `filters[].operator` | list | no |  |
| `filters[].value` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `excludeOrderDetails` | boolean | no | Exclude line details from the response. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MarketTime API returns.

## Native endpoint

Through the native MarketTime API, this operation is `POST /mtpublic/api/v1/:whoAmI/orders/get` (base URL `https://publicapi.markettime.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/pull-orders.md) for the provider-specific parameters and requirements.

