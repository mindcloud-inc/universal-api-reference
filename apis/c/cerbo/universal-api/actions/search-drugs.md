# Cerbo: Search Drugs

Finds drugs in Cerbo by search term.

```
GET https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/search-drugs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/search-drugs?connectionId=$CONNECTION_ID&limit=25&offset=0&term=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "term": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/search-drugs?${params}`, {
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
| `term` | string | yes | Search term for drug name |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `favorites-only` | boolean | no | Return only drugs from provider's favorites list Default: `true`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cerbo API returns.

## Native endpoint

Through the native Cerbo API, this operation is `GET /drugs/search/:term` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-drugs.md) for the provider-specific parameters and requirements.

