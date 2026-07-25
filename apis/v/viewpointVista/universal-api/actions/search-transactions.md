# Viewpoint Vista: Search Transactions



```
GET https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/search-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Vista `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/search-transactions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/search-transactions?${params}`, {
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
| `modifiedUtcAfter` | date | no | Returns transactions modified after this timestamp. Format: yyyy-MM-ddThh:mm:ss.fffffffZ. |
| `modifiedUtcBefore` | date | no | Returns transactions modified before this timestamp. Format: yyyy-MM-ddThh:mm:ss.fffffffZ. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Viewpoint Vista API returns.

## Native endpoint

Through the native Viewpoint Vista API, this operation is `POST v1/direct/subscribers/{{credentials.subscriberCode}}/vista/ar/2/data/transactions/cache/search` (base URL `https://api.xchange.trimble.com/connect/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-transactions.md) for the provider-specific parameters and requirements.

