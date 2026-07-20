# GrowthBook: Create a single metric

Creates a new metric in GrowthBook.

```
POST https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-metric
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-metric" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "datasourceId": "sample_id_1",
  "name": "sample",
  "type": "sample"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-metric', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "datasourceId": "sample_id_1",
    "name": "sample",
    "type": "sample"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `datasourceId` | string | yes | ID for the [DataSource](#tag/DataSource_model) Default: `sample_id_1`. |
| `managedBy` | string | no | Where this metric must be managed from. If not set (empty string), it can be managed from anywhere. If set to "api", it can be managed via the API only. |
| `owner` | string | no | The userId or email address of the owner. If an email address is provided, it will be used to look up the userId of the matching organization member. If an ID is provided, it will be validated as existing in the organization. |
| `name` | string | yes | Name of the metric Default: `sample`. |
| `description` | string | no | Description of the metric |
| `type` | string | yes | Type of metric. See [Metrics documentation](/app/metrics/legacy) Default: `sample`. |
| `tags` | list<string> | no | List of tags |
| `projects` | list<string> | no | List of project IDs for projects that can access this metric |
| `archived` | boolean | no |  |
| `behavior` | object | no |  |
| `sql` | object | no | Preferred way to define SQL. Only one of `sql`, `sqlBuilder` or `mixpanel` allowed, and at least one must be specified. |
| `sqlBuilder` | object | no | An alternative way to specify a SQL metric, rather than a full query. Using `sql` is preferred to `sqlBuilder`. Only one of `sql`, `sqlBuilder` or `mixpanel` allowed, and at least one must be specified. |
| `mixpanel` | object | no | Only use for MixPanel (non-SQL) Data Sources. Only one of `sql`, `sqlBuilder` or `mixpanel` allowed, and at least one must be specified. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "metric": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `metric` | object |  |

## Native endpoint

Through the native GrowthBook API, this operation is `POST /metrics` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-metric.md) for the provider-specific parameters and requirements.

