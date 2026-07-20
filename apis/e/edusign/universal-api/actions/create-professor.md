# Edusign: Create Professor

Creates a new professor in Edusign.

```
POST https://connect.mindcloud.co/v1/universal/edusign/latest/actions/create-professor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Edusign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/edusign/latest/actions/create-professor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "professor": {},
  "professor.firstname": "Ava",
  "professor.lastname": "Chen",
  "professor.email": "ava@example.com",
  "dontSendCredentials": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/edusign/latest/actions/create-professor', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "professor": {},
    "professor.firstname": "Ava",
    "professor.lastname": "Chen",
    "professor.email": "ava@example.com",
    "dontSendCredentials": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `professor` | object | yes |  |
| `professor.firstname` | string | yes | Firstname of the professor |
| `professor.lastname` | string | yes | Lastname of the professor |
| `professor.email` | string | yes | Email of the professor |
| `professor.speciality` | string | no | Speciality of the professor |
| `professor.apiId` | string | no | API ID of the professor |
| `professor.apiType` | string | no | API type of the professor |
| `professor.phone` | string | no | Phone of the professor |
| `dontSendCredentials` | boolean | yes | If true, the credentials won't be sent to the professor |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `professor.tags[]` | array<string> | no |  |
| `professor.tags[]` | array<string> | no |  |
| `professor.variables[]` | array<object> | no |  |
| `professor.variables[]` | array<object> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {
        "id": "string",
        "type": "string"
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object |  |
| `result.id` | string |  |
| `result.type` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Edusign API, this operation is `POST /v1/professor` (base URL `https://ext.edusign.fr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-professor.md) for the provider-specific parameters and requirements.

