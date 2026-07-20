# GrowthBook: Create a Data Source based visualization

Creates a data source visualization in GrowthBook.

```
POST https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-data-source-exploration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-data-source-exploration" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "datasource": "sample",
  "dimensions[]": [
    "sample"
  ],
  "chartType": "sample",
  "dateRange": "2026-01-01T00:00:00.000Z",
  "type": "sample",
  "dataset": {
    "sample": "value"
  }
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-data-source-exploration', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "datasource": "sample",
    "dimensions[]": ["sample"],
    "chartType": "sample",
    "dateRange": "2026-01-01T00:00:00.000Z",
    "type": "sample",
    "dataset": {"sample":"value"}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cache` | string | no | Controls cache behavior for this exploration: `preferred` (default) returns a cached result if one exists, otherwise runs a new query; `never` always runs a new query, ignoring any cached results; `required` only returns a cached result, if none exists returns exploration: null with a message |
| `datasource` | string | yes | ID of the datasource to query Default: `sample`. |
| `dimensions[]` | array<object> | yes | Default: `["sample"]`. |
| `chartType` | string | yes | Default: `sample`. |
| `dateRange` | object | yes | Default: `2026-01-01T00:00:00.000Z`. |
| `type` | string | yes | Default: `sample`. |
| `dataset` | object | yes | Default: `{"sample":"value"}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "exploration": {},
      "explorationUrl": "https://example.com",
      "message": "string",
      "query": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `exploration` | object |  |
| `explorationUrl` | string | A direct link to view this exploration in the GrowthBook Application. |
| `message` | string | Present when `exploration` is null, explaining why no result was returned. |
| `query` | object |  |

## Native endpoint

Through the native GrowthBook API, this operation is `POST /product-analytics/data-source-exploration` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-data-source-exploration.md) for the provider-specific parameters and requirements.

