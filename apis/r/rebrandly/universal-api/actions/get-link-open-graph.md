# Rebrandly: Get Link OpenGraph

Retrieves OpenGraph metadata for a link in Rebrandly.

```
GET https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/get-link-open-graph
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rebrandly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/get-link-open-graph?connectionId=$CONNECTION_ID&id=be1dc193df104ee9b9878f528a933490" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "be1dc193df104ee9b9878f528a933490"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/get-link-open-graph?${params}`, {
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
| `id` | string | yes | Unique identifier of the branded short link. Example: `be1dc193df104ee9b9878f528a933490`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rebrandly API returns.

## Native endpoint

Through the native Rebrandly API, this operation is `GET /links/:id/opengraph` (base URL `https://api.rebrandly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-link-open-graph.md) for the provider-specific parameters and requirements.

