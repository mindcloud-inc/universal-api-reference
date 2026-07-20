# Cerbo: Delete Patient Specialist

Deletes a patient specialist from Cerbo.

```
DELETE https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/delete-patient-specialist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/delete-patient-specialist?connectionId=$CONNECTION_ID&patient_id=1&patient_specialist_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "patient_id": "1",
  "patient_specialist_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/delete-patient-specialist?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `patient_id` | number | yes | The patient ID |
| `patient_specialist_id` | number | yes | The patient-specialist association ID (not the specialist ID) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `result` | boolean |  |

## Native endpoint

Through the native Cerbo API, this operation is `DELETE /patients/:patient_id/specialists/:patient_specialist_id` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-patient-specialist.md) for the provider-specific parameters and requirements.

