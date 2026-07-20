# Cerbo: Queue Patient Supplement

Queues a patient supplement request in Cerbo.

```
POST https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/queue-patient-supplement
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/queue-patient-supplement" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "supplement_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/queue-patient-supplement', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "supplement_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `patient_id` | number | no |  |
| `supplement_id` | number | yes | An integer identifier for a supplement as returned from a /v1/supplements/search/:term query. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `enqueue` | boolean | no | (true by default) If true, the system will insert the supplement into the active patient portal queue so that the clinic is notified and can review the proposed addition. This replicates the functionality of the patient portal queue. |
| `notes` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cerbo API returns.

## Native endpoint

Through the native Cerbo API, this operation is `POST /patients/:patient_id/supplements` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/queue-patient-supplement.md) for the provider-specific parameters and requirements.

