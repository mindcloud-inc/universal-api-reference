# Cerbo: List Patient Past Medical History

Retrieves patient past medical history from Cerbo.

```
GET https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-patient-past-medical-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-patient-past-medical-history?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-patient-past-medical-history?${params}`, {
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
| `patient_id` | number | no | ID of patient |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addedby": "string",
      "code": "string",
      "created": "string",
      "display_name": "Ava Chen",
      "encounter_id": 1,
      "icd_version": "string",
      "id": "string",
      "name": "Ava Chen",
      "object": "string",
      "problem_status": "string",
      "url_encounter": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addedby` | string |  |
| `code` | string |  |
| `created` | string |  |
| `display_name` | string |  |
| `encounter_id` | number |  |
| `icd_version` | string |  |
| `id` | string |  |
| `name` | string |  |
| `object` | string |  |
| `problem_status` | string |  |
| `url_encounter` | number |  |

## Native endpoint

Through the native Cerbo API, this operation is `GET /patients/:patient_id/pmh` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-patient-past-medical-history.md) for the provider-specific parameters and requirements.

