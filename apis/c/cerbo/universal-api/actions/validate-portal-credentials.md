# Cerbo: Validate Portal Credentials

Validates Cerbo patient portal login credentials.

```
GET https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/validate-portal-credentials
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/validate-portal-credentials?connectionId=$CONNECTION_ID&username=Ava%20Chen&password=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "username": "Ava Chen",
  "password": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/validate-portal-credentials?${params}`, {
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
| `username` | string | yes | The patient's username that they use to login to your patient portal |
| `password` | string | yes | The patient's password that they use to login to your patient portal |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "patient_details": {
        "email_address": "ava@example.com",
        "first_name": "Ava",
        "id": 1,
        "last_name": "Chen",
        "status": "string"
      },
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
| `patient_details` | object |  |
| `patient_details.email_address` | string |  |
| `patient_details.first_name` | string |  |
| `patient_details.id` | number |  |
| `patient_details.last_name` | string |  |
| `patient_details.status` | string |  |
| `result` | boolean |  |

## Native endpoint

Through the native Cerbo API, this operation is `POST /patients/portal/validate_credentials` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-portal-credentials.md) for the provider-specific parameters and requirements.

