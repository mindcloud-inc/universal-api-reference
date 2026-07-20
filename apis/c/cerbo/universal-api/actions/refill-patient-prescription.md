# Cerbo: Refill Patient Prescription

Queues a patient prescription refill in Cerbo.

```
PUT https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/refill-patient-prescription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/refill-patient-prescription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "original_prescription_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/refill-patient-prescription', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "original_prescription_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `patient_id` | number | no | ID of patient |
| `original_prescription_id` | number | yes | An integer identifier for an existing prescription for this patient as returned from a /v1/patients/:patient_id/rxs GET query. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `notes` | string | no |  |
| `agreed_to_terms` | string | no | A string value representing agreement to terms. If not set, defaults to "No terms agreed to". |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cerbo API returns.

## Native endpoint

Through the native Cerbo API, this operation is `POST /patients/:patient_id/rxs/refill` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/refill-patient-prescription.md) for the provider-specific parameters and requirements.

