# Cerbo: Update Patient

Updates an existing patient in Cerbo.

```
PUT https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/update-patient
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/update-patient" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "patient_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/update-patient', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "patient_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `patient_id` | number | yes | ID of the patient to update |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `first_name` | string | no |  |
| `last_name` | string | no |  |
| `dob` | string | no | YYYY-MM-DD |
| `sex` | string | no | must be 'M', 'F', or '?' |
| `inactive` | string | no | Sets the patient status. Accepts the following values: \| Value \| Result \| \|---\|---\| \| `"prospective"` or `"-1"` \| Prospective patient \| \| `"0"`, empty, or omitted \| Active patient (default) \| \| `"inactive"` or `"1"` \| Inactive patient \| \| `"deceased"` or `"dead"` or `"2"` \| Deceased patient \| **Important — GET response behavior:** When reading patient data via GET, the `inactive` field is cast to a boolean rather than returning the original value. This means: \| Stored status \| `inactive` in GET \| `patient_status_description` in GET \| \|---\|---\|---\| \| Prospective (`-1`) \| `true` \| `"prospective"` \| \| Active (`0`) \| `false` \| `"active"` \| \| Inactive (`1`) \| `true` \| `"inactive"` \| \| Deceased (`2`) \| `true` \| `"deceased"` \| Because `inactive` returns `true` for prospective, inactive, and deceased patients alike, you **must** use the `patient_status_description` field to determine the actual status. This is a known legacy serialization issue where the create/update and read representations differ. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cerbo API returns.

## Native endpoint

Through the native Cerbo API, this operation is `PATCH /patients/:patient_id` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-patient.md) for the provider-specific parameters and requirements.

