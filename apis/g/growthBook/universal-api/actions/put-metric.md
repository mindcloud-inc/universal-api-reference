# GrowthBook: Update a metric

Updates an existing metric in GrowthBook.

```
PUT https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/put-metric
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/put-metric" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "prj_19g6smo332up7"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/put-metric', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "prj_19g6smo332up7"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The id of the requested resource Default: `prj_19g6smo332up7`. |
| `managedBy` | string | no | Where this metric must be managed from. If not set (empty string), it can be managed from anywhere. If set to "api", it can be managed via the API only. Please note that we have deprecated support for setting the managedBy property to "admin". Your existing Legacy Metrics with this value will continue to work, but we suggest migrating to Fact Metrics instead. |
| `owner` | string | no | The userId or email address of the owner. If an email address is provided, it will be used to look up the userId of the matching organization member. If an ID is provided, it will be validated as existing in the organization. |
| `name` | string | no | Name of the metric |
| `description` | string | no | Description of the metric |
| `type` | string | no | Type of metric. See [Metrics documentation](/app/metrics/legacy) |
| `tags` | list<string> | no | List of tags |
| `projects` | list<string> | no | List of project IDs for projects that can access this metric |
| `archived` | boolean | no |  |
| `behavior` | object | no |  |
| `sql` | object | no | Preferred way to define SQL. Only one of `sql`, `sqlBuilder` or `mixpanel` allowed. |
| `sqlBuilder` | object | no | An alternative way to specify a SQL metric, rather than a full query. Using `sql` is preferred to `sqlBuilder`. Only one of `sql`, `sqlBuilder` or `mixpanel` allowed |
| `mixpanel` | object | no | Only use for MixPanel (non-SQL) Data Sources. Only one of `sql`, `sqlBuilder` or `mixpanel` allowed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "updatedId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `updatedId` | string |  |

## Native endpoint

Through the native GrowthBook API, this operation is `PUT /metrics/:id` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/put-metric.md) for the provider-specific parameters and requirements.

