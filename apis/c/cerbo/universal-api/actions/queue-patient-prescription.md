# Cerbo: Queue Patient Prescription

Queues a patient prescription request in Cerbo.

```
POST https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/queue-patient-prescription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/queue-patient-prescription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "drug_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/queue-patient-prescription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "drug_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `patient_id` | number | no | ID of patient |
| `drug_id` | number | yes | An integer identifier for a drug as returned from a /v1/drugs/search/:term query. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `enqueue` | boolean | no | (true by default) If true, the system will insert the drug into the active patient portal queue so that the clinic is notified and can review the proposed addition. This replicates the functionality of the patient portal queue. |
| `notes` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cerbo API returns.

## Native endpoint

Through the native Cerbo API, this operation is `POST /patients/:patient_id/rxs` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/queue-patient-prescription.md) for the provider-specific parameters and requirements.

