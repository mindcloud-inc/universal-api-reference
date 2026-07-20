# Cerbo: Add Patient Laboratory

Adds a patient laboratory record in Cerbo.

```
POST https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/add-patient-laboratory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/add-patient-laboratory" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "patient_id": 1,
  "laboratory_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/add-patient-laboratory', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "patient_id": 1,
    "laboratory_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `patient_id` | number | yes | ID of the patient |
| `laboratory_id` | number | yes | An integer, the laboratory ID to add. See the "Facility Endpoints" documentation for how to find the ID in the master laboratories database |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `priority_order` | number | no | An integer representing where in the patient's laboratories list this entry should go (lowest number is considered the first/preferred listing). If null, the system will look at set_as_primary instead. |
| `set_as_primary` | boolean | no | A boolean value representing if this should be added as the patient's new preferred listing, or just added to the bottom of the list. If priority_order is set, this argument will be ignored. |
| `note` | string | no | A string, 255 character max |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cerbo API returns.

## Native endpoint

Through the native Cerbo API, this operation is `POST /patients/:patient_id/laboratories` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-patient-laboratory.md) for the provider-specific parameters and requirements.

