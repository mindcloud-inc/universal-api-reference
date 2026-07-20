# Nuclino: Search items and collections

Finds items and collections in Nuclino by search query.

```
GET https://connect.mindcloud.co/v1/universal/nuclino/latest/actions/search-items-and-collections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nuclino `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nuclino/latest/actions/search-items-and-collections?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nuclino/latest/actions/search-items-and-collections?${params}`, {
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
| `search` | string | no |  |
| `teamId` | string | no |  |
| `workspaceId` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Nuclino API returns.

## Native endpoint

Through the native Nuclino API, this operation is `GET /items` (base URL `https://api.nuclino.com/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-items-and-collections.md) for the provider-specific parameters and requirements.

