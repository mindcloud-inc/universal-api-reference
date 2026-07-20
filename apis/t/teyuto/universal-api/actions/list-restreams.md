# Teyuto: List Restreams

Retrieves all restreams from a Teyuto channel.

```
GET https://connect.mindcloud.co/v1/universal/teyuto/latest/actions/list-restreams
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teyuto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teyuto/latest/actions/list-restreams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teyuto/latest/actions/list-restreams?${params}`, {
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
| `page` | number | no | Page of restreams to return. |
| `pageSize` | number | no | Number of restreams per page. |
| `search` | string | no | Search restreams by ID or name. |
| `order` | string | no | Sort order for restream results. |
| `liveNow` | boolean | no | Return only restreams that are live right now. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Teyuto API returns.

## Native endpoint

Through the native Teyuto API, this operation is `GET /restreams` (base URL `https://api.teyuto.tv/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-restreams.md) for the provider-specific parameters and requirements.

