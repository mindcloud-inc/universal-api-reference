# Otiom: Get Patient Homebase

Retrieves a patient's homebase from Otiom.

```
GET https://connect.mindcloud.co/v1/universal/otiom/latest/actions/get-patient-homebase
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Otiom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/otiom/latest/actions/get-patient-homebase?connectionId=$CONNECTION_ID&patientId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "patientId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/otiom/latest/actions/get-patient-homebase?${params}`, {
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
      "homebases": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `homebases` | array |  |

## Native endpoint

Through the native Otiom API, this operation is `GET /api/patients/:patientid/homebase/` (base URL `https://api.otiom.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-patient-homebase.md) for the provider-specific parameters and requirements.

