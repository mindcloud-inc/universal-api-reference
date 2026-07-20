# RocketReach: Search Universal Companies

Finds companies in RocketReach Universal search.

```
GET https://connect.mindcloud.co/v1/universal/rocketReach/latest/actions/search-universal-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RocketReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rocketReach/latest/actions/search-universal-companies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rocketReach/latest/actions/search-universal-companies?${params}`, {
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
| `start` | number | no | Paginate through search results by returning results starting from this value, counting from 1. Default: `1`. Example: `1`. |
| `pageSize` | number | no | Maximum number of search results to return per page. Default: `100`. Example: `100`. |
| `orderBy` | string | no | Specifies the ordering of search results. Allowed values: relevance, popularity, score. Default: `relevance`. Example: `relevance`. |
| `query` | object | no | RocketReach universal company search filter object. Supply the exact documented filter keys inside this object. Example: `[object Object]`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native RocketReach API returns.

## Native endpoint

Through the native RocketReach API, this operation is `POST /universal/company/search` (base URL `https://api.rocketreach.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-universal-companies.md) for the provider-specific parameters and requirements.

