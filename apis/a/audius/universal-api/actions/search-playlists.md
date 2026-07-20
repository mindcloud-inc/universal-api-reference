# Audius: Search Playlists

Finds playlists in Audius by query.

```
GET https://connect.mindcloud.co/v1/universal/audius/latest/actions/search-playlists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Audius `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/audius/latest/actions/search-playlists?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/audius/latest/actions/search-playlists?${params}`, {
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
| `query` | string | yes |  |
| `limit` | number | no |  |
| `offset` | number | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Audius API returns.

## Native endpoint

Through the native Audius API, this operation is `GET /playlists/search` (base URL `https://api.audius.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-playlists.md) for the provider-specific parameters and requirements.

