# GrowthBook: Update a single dashboard

Updates an existing dashboard in GrowthBook.

```
PUT https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/update-dashboard
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/update-dashboard" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "prj_19g6smo332up7"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/update-dashboard', {
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
| `id` | string | yes | Default: `prj_19g6smo332up7`. |
| `title` | string | no | The display name of the Dashboard |
| `editLevel` | string | no | Dashboards that are "published" are editable by organization members with appropriate permissions |
| `shareLevel` | string | no | General Dashboards only. Dashboards that are "published" are viewable by organization members with appropriate permissions |
| `enableAutoUpdates` | boolean | no | If enabled for a General Dashboard, also requires an updateSchedule |
| `updateSchedule` | object | no |  |
| `projects` | list<string> | no | General Dashboards only, Experiment Dashboards use the experiment's projects |
| `blocks[]` | array<object> | no |  |

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

Through the native GrowthBook API, this operation is `PUT /dashboards/:id` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-dashboard.md) for the provider-specific parameters and requirements.

