# Library of Congress: Search Personal Narratives

Finds personal narratives in Library of Congress.

```
GET https://connect.mindcloud.co/v1/universal/libraryOfCongress/latest/actions/search-personal-narratives
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Library of Congress `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/libraryOfCongress/latest/actions/search-personal-narratives?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/libraryOfCongress/latest/actions/search-personal-narratives?${params}`, {
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
| `query` | string | no | Full-text search query. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `attributes` | string | no | Comma-separated response sections to request. |
| `sortBy` | string | no | Sort order for search results. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Library of Congress API returns.

## Native endpoint

Through the native Library of Congress API, this operation is `GET /search/` (base URL `https://www.loc.gov`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-personal-narratives.md) for the provider-specific parameters and requirements.

