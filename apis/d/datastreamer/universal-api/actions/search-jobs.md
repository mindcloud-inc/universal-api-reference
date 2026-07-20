# Datastreamer: Search Jobs

Finds jobs in Datastreamer by Lucene query.

```
GET https://connect.mindcloud.co/v1/universal/datastreamer/latest/actions/search-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datastreamer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datastreamer/latest/actions/search-jobs?connectionId=$CONNECTION_ID&query=%5Bobject%20Object%5D&query.query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "[object Object]",
  "query.query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datastreamer/latest/actions/search-jobs?${params}`, {
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
| `query` | object | yes | Search request payload. |
| `query.query` | string | yes | Lucene query string used to search job history. |
| `query.from` | number | no | Zero-based starting offset for the search results. Default: `0`. |
| `query.size` | number | no | Maximum number of jobs to return. Default: `100`. |
| `query.track_total_hits` | boolean | no | Return the total number of matching jobs. Default: `false`. |
| `query.sort[]` | array<object> | no | Sort instructions for the search. |
| `query.sort[].field` | string | no | Job field used for sorting. Default: `updated`. |
| `query.sort[].order` | string | no | Sort order, ASC or DESC. Default: `DESC`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Datastreamer API returns.

## Native endpoint

Through the native Datastreamer API, this operation is `POST /api/pipelines/jobs/search` (base URL `https://api.platform.datastreamer.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-jobs.md) for the provider-specific parameters and requirements.

