# GrowthBook: Create a single dashboard

Creates a new dashboard in GrowthBook.

```
POST https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/create-dashboard
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/create-dashboard" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "sample",
  "editLevel": "sample",
  "shareLevel": "sample",
  "enableAutoUpdates": "2026-01-01T00:00:00.000Z",
  "blocks[]": [
    "sample"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/create-dashboard', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "sample",
    "editLevel": "sample",
    "shareLevel": "sample",
    "enableAutoUpdates": "2026-01-01T00:00:00.000Z",
    "blocks[]": ["sample"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | The display name of the Dashboard Default: `sample`. |
| `editLevel` | string | yes | Dashboards that are "published" are editable by organization members with appropriate permissions Default: `sample`. |
| `shareLevel` | string | yes | General Dashboards only. Dashboards that are "published" are viewable by organization members with appropriate permissions Default: `sample`. |
| `enableAutoUpdates` | boolean | yes | If enabled for a General Dashboard, also requires an updateSchedule Default: `2026-01-01T00:00:00.000Z`. |
| `updateSchedule` | object | no |  |
| `experimentId` | string | no | The parent experiment for an Experiment Dashboard, or undefined for a general dashboard |
| `projects` | list<string> | no | General Dashboards only, Experiment Dashboards use the experiment's projects |
| `blocks[]` | array<object> | yes | Default: `["sample"]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dashboard": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dashboard` | object |  |

## Native endpoint

Through the native GrowthBook API, this operation is `POST /dashboards` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-dashboard.md) for the provider-specific parameters and requirements.

