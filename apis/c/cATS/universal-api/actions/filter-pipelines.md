# CATS: Filter Pipelines

Finds pipelines in CATS by filter criteria.

```
GET https://connect.mindcloud.co/v1/universal/cATS/latest/actions/filter-pipelines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CATS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cATS/latest/actions/filter-pipelines?connectionId=$CONNECTION_ID&field=candidate_id&filter=exactly&value=411876208" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "field": "candidate_id",
  "filter": "exactly",
  "value": "411876208"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cATS/latest/actions/filter-pipelines?${params}`, {
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
| `field` | string | yes | The field to filter on. Example: `candidate_id`. |
| `filter` | string | yes | The filter operator to use. Example: `exactly`. |
| `value` | string | yes | The value to filter by. Example: `411876208`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CATS API returns.

## Native endpoint

Through the native CATS API, this operation is `POST /pipelines/search` (base URL `https://api.catsone.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/filter-pipelines.md) for the provider-specific parameters and requirements.

