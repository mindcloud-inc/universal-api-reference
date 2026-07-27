# Google Search Console: Query Search Analytics



```
GET https://connect.mindcloud.co/v1/universal/googleSearchConsole/latest/actions/query-search-analytics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Search Console `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleSearchConsole/latest/actions/query-search-analytics?connectionId=$CONNECTION_ID&limit=25&offset=0&siteUrl=https%3A%2F%2Fexample.com&startDate=YYYY-MM-DD&endDate=YYYY-MM-DD" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "siteUrl": "https://example.com",
  "startDate": "YYYY-MM-DD",
  "endDate": "YYYY-MM-DD"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleSearchConsole/latest/actions/query-search-analytics?${params}`, {
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
| `siteUrl` | list<string> | yes | The Search Console property URL to query, such as a URL-prefix property or a sc-domain property. |
| `startDate` | date | yes | Start date of the requested date range in YYYY-MM-DD format, in Pacific Time. Example: `YYYY-MM-DD`. |
| `endDate` | date | yes | End date of the requested date range in YYYY-MM-DD format, in Pacific Time. Example: `YYYY-MM-DD`. |
| `dimensions[]` | array<string> | no | Optional list of dimensions to group rows by, such as country, device, page, query, date, or hour. |
| `type` | list<string> | no | Optional search result type filter. Docs list web, image, video, news, googleNews, and discover. One of: `discover`, `googleNews`, `image`, `news`, `video`, `web`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dimensionFilterGroups[]` | array<object> | no | Optional dimension filter groups payload matching the Search Analytics API request body format. |
| `aggregationType` | list<string> | no | Optional aggregation type. Docs list auto, byPage, byProperty, and byNewsShowcasePanel with scope restrictions. One of: `auto`, `byNewsShowcasePanel`, `byPage`, `byProperty`. |
| `dataState` | list<string> | no | Optional data freshness mode. Docs list final, all, and hourly_all. One of: `all`, `final`, `hourly_all`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Google Search Console API returns.

## Native endpoint

Through the native Google Search Console API, this operation is `POST sites/:siteUrl/searchAnalytics/query` (base URL `https://www.googleapis.com/webmasters/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/query-search-analytics.md) for the provider-specific parameters and requirements.

