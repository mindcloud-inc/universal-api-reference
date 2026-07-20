# GoSquared: List Tagged Visitors

Retrieves tagged visitors for a GoSquared site.

```
GET https://connect.mindcloud.co/v1/universal/goSquared/latest/actions/list-tagged-visitors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoSquared `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goSquared/latest/actions/list-tagged-visitors?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goSquared/latest/actions/list-tagged-visitors?${params}`, {
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
| `presenter` | string | no | Modifies the response data structure. Accepted values: plain, indexed. Default: `plain`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GoSquared API returns.

## Native endpoint

Through the native GoSquared API, this operation is `GET account/v1/taggedVisitors` (base URL `https://api.gosquared.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tagged-visitors.md) for the provider-specific parameters and requirements.

