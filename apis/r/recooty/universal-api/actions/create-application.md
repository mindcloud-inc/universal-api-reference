# Recooty: Create Application



```
POST https://connect.mindcloud.co/v1/universal/recooty/latest/actions/create-application
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recooty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/recooty/latest/actions/create-application" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "jobId": "string",
  "firstName": "Ava",
  "lastName": "Chen",
  "email": "ava@example.com",
  "mobileNumber": "string",
  "resume": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recooty/latest/actions/create-application', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "jobId": "string",
    "firstName": "Ava",
    "lastName": "Chen",
    "email": "ava@example.com",
    "mobileNumber": "string",
    "resume": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `jobId` | string | yes | The Recooty job ID. |
| `firstName` | string | yes | Applicant first name. |
| `lastName` | string | yes | Applicant last name. |
| `email` | string | yes | Applicant email address. |
| `mobileNumber` | string | yes | Applicant mobile number. |
| `resume` | string | yes | Resume file input or file URL, depending on your runtime connector input. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "application": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `application` | object | The created application record. |

## Native endpoint

Through the native Recooty API, this operation is `POST /v1/jobs/{{jobId}}/application` (base URL `https://standaloneapi.recooty.app/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-application.md) for the provider-specific parameters and requirements.

