# Edusign: Get Student By Email

Finds a student in Edusign by email address.

```
GET https://connect.mindcloud.co/v1/universal/edusign/latest/actions/get-student-by-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Edusign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/edusign/latest/actions/get-student-by-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/edusign/latest/actions/get-student-by-email?${params}`, {
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
| `email` | string | yes | Student email |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {
        "apiId": "string",
        "apiType": "string",
        "badgeId": "string",
        "company": "string",
        "dateCreated": "string",
        "dateUpdated": "string",
        "email": "ava@example.com",
        "fileNumber": "string",
        "firstname": "Ava",
        "groups": [
          "string"
        ],
        "hidden": 1,
        "id": "string",
        "language": "string",
        "lastname": "Chen",
        "multiAccountLoginCode": 1,
        "newPasswordNeeded": 1,
        "phone": "string",
        "photo": "string",
        "schoolId": "string",
        "signatureId": "string",
        "studentFollowerId": [
          "string"
        ],
        "tags": [
          "string"
        ],
        "trainingIds": [
          "string"
        ],
        "trainingName": "Ava Chen",
        "username": "Ava Chen",
        "variables": [
          {
            "name": "Ava Chen",
            "value": "string"
          }
        ]
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
| `result.apiId` | string |  |
| `result.apiType` | string |  |
| `result.badgeId` | string |  |
| `result.company` | string |  |
| `result.dateCreated` | string |  |
| `result.dateUpdated` | string |  |
| `result.email` | string |  |
| `result.fileNumber` | string |  |
| `result.firstname` | string |  |
| `result.groups` | array<string> |  |
| `result.hidden` | number |  |
| `result.id` | string |  |
| `result.language` | string |  |
| `result.lastname` | string |  |
| `result.multiAccountLoginCode` | number |  |
| `result.newPasswordNeeded` | number |  |
| `result.phone` | string |  |
| `result.photo` | string |  |
| `result.schoolId` | string |  |
| `result.signatureId` | string |  |
| `result.studentFollowerId` | array<string> |  |
| `result.tags` | array<string> |  |
| `result.trainingIds` | array<string> |  |
| `result.trainingName` | string |  |
| `result.username` | string |  |
| `result.variables` | array<object> |  |
| `result.variables[].name` | string |  |
| `result.variables[].value` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Edusign API, this operation is `GET /v1/student/by-email/:email` (base URL `https://ext.edusign.fr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-student-by-email.md) for the provider-specific parameters and requirements.

