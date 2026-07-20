# GrowthBook: Create a single metricGroup

Creates a new metric group in GrowthBook.

```
POST https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/create-metric-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/create-metric-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "sample",
  "description": "sample",
  "projects": [
    "sample"
  ],
  "metrics": [
    "sample"
  ],
  "datasource": "sample"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/create-metric-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "sample",
    "description": "sample",
    "projects": ["sample"],
    "metrics": ["sample"],
    "datasource": "sample"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Default: `sample`. |
| `description` | string | yes | Default: `sample`. |
| `tags` | list<string> | no |  |
| `projects` | list<string> | yes | Default: `["sample"]`. |
| `metrics` | list<string> | yes | Default: `["sample"]`. |
| `datasource` | string | yes | Default: `sample`. |
| `owner` | string | no | The userId or email address of the owner. If an email address is provided, it will be used to look up the userId of the matching organization member. If an ID is provided, it will be validated as existing in the organization. |
| `archived` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "metricGroup": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `metricGroup` | object |  |

## Native endpoint

Through the native GrowthBook API, this operation is `POST /metric-groups` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-metric-group.md) for the provider-specific parameters and requirements.

