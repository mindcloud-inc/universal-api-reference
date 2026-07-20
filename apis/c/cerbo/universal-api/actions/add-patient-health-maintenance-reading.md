# Cerbo: Add Patient Health Maintenance Reading

Adds a patient health maintenance reading in Cerbo.

```
POST https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/add-patient-health-maintenance-reading
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/add-patient-health-maintenance-reading" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "patient_id": 1,
  "health_maintenance_id": 1,
  "date": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/add-patient-health-maintenance-reading', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "patient_id": 1,
    "health_maintenance_id": 1,
    "date": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `patient_id` | number | yes | ID of patient |
| `health_maintenance_id` | number | yes | ID of health maintenance entry *See “HEALTH MAINTENANCE ENDPOINTS” documentation to get definitions from the master health maintenance trackers list |
| `date` | string | yes | A string specifying the date of the health maintenance tracker. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `notes` | number | no | A string |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cerbo API returns.

## Native endpoint

Through the native Cerbo API, this operation is `POST /patients/:patient_id/health_maintenance/:health_maintenance_id` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-patient-health-maintenance-reading.md) for the provider-specific parameters and requirements.

