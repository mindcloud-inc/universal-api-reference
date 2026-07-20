# Fingertip: List Orders



```
GET https://connect.mindcloud.co/v1/universal/fingertip/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fingertip `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fingertip/latest/actions/list-orders?connectionId=$CONNECTION_ID&limit=25&offset=0&site=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "site": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fingertip/latest/actions/list-orders?${params}`, {
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
| `site` | string | yes | ID of the site to list orders for. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Fingertip API returns.

## Native endpoint

Through the native Fingertip API, this operation is `GET /v1/orders` (base URL `https://api.fingertip.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

