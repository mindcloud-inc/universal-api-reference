# Cerbo: Create Patient Specialist

Creates a patient specialist record in Cerbo.

```
POST https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/create-patient-specialist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/create-patient-specialist" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "patient_id": 1,
  "specialist_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/create-patient-specialist', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "patient_id": 1,
    "specialist_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `patient_id` | number | yes | The patient ID |
| `specialist_id` | number | yes | The specialist ID from the master specialists database. Use the facilities/specialists endpoints to find valid IDs. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `priority_order` | number | no | Position in the patient's specialist list (lower = higher priority). If provided, `set_as_primary` is ignored. |
| `set_as_primary` | boolean | no | If true, adds to top of list (priority). If false, adds to bottom. Only used when `priority_order` is not provided. |
| `note` | string | no | Optional note about this specialist for the patient (max 255 characters) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "note": "string",
      "priority_order": 1,
      "specialist_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `id` | number |  |
| `note` | string |  |
| `priority_order` | number |  |
| `specialist_id` | number |  |

## Native endpoint

Through the native Cerbo API, this operation is `POST /patients/:patient_id/specialists` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-patient-specialist.md) for the provider-specific parameters and requirements.

