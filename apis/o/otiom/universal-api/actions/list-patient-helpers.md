# Otiom: List Patient Helpers

Retrieves helpers for a patient from Otiom.

```
GET https://connect.mindcloud.co/v1/universal/otiom/latest/actions/list-patient-helpers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Otiom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/otiom/latest/actions/list-patient-helpers?connectionId=$CONNECTION_ID&patientId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "patientId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/otiom/latest/actions/list-patient-helpers?${params}`, {
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
| `patientId` | number | yes | A unique integer value identifying this patient. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string |  |
| `username` | string |  |

## Native endpoint

Through the native Otiom API, this operation is `GET /api/patients/:patientid/helpers/` (base URL `https://api.otiom.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-patient-helpers.md) for the provider-specific parameters and requirements.

