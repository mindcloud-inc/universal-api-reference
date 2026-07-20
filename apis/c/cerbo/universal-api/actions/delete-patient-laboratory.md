# Cerbo: Delete Patient Laboratory

Deletes a patient laboratory from Cerbo.

```
DELETE https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/delete-patient-laboratory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/delete-patient-laboratory?connectionId=$CONNECTION_ID&patient_id=1&patient_laboratory_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "patient_id": "1",
  "patient_laboratory_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/delete-patient-laboratory?${params}`, {
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
| `patient_id` | number | yes | ID of the patient |
| `patient_laboratory_id` | number | yes | ID of the patient laboratory association |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cerbo API returns.

## Native endpoint

Through the native Cerbo API, this operation is `DELETE /patients/:patient_id/laboratories/:patient_laboratory_id` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-patient-laboratory.md) for the provider-specific parameters and requirements.

