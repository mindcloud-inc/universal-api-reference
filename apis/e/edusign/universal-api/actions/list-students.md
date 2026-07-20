# Edusign: List Students

Retrieves students from Edusign.

```
GET https://connect.mindcloud.co/v1/universal/edusign/latest/actions/list-students
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Edusign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/edusign/latest/actions/list-students?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/edusign/latest/actions/list-students?${params}`, {
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
| `page` | string | no | Query param for pagination, starts at page "0" |
| `limit` | string | no | Number of students per page |
| `updatedAfter` | string | no | Filter students updated after this date (ISO format) |
| `search` | string | no | Search in student's firstname, lastname and email |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": [
        {
          "apiId": "string",
          "apiType": "string",
          "badgeId": "string",
          "company": "string",
          "dateCreated": "string",
          "dateUpdated": "string",
          "email": "ava@example.com",
          "fileNumber": "string",
          "firstname": "Ava",
          "hidden": 1,
          "id": "string",
          "language": "string",
          "lastname": "Chen",
          "multiAccountLoginCode": 1,
          "newPasswordNeeded": 1,
          "newPasswordToken": "string",
          "password": "string",
          "phone": "string",
          "photo": "string",
          "pushToken": "string",
          "schoolId": "string",
          "signatureId": "string",
          "studentFollowerId": [
            "string"
          ],
          "tags": [
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
        }
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | array<object> |  |
| `result[].apiId` | string |  |
| `result[].apiType` | string |  |
| `result[].badgeId` | string |  |
| `result[].company` | string |  |
| `result[].dateCreated` | string |  |
| `result[].dateUpdated` | string |  |
| `result[].email` | string |  |
| `result[].fileNumber` | string |  |
| `result[].firstname` | string |  |
| `result[].hidden` | number |  |
| `result[].id` | string |  |
| `result[].language` | string |  |
| `result[].lastname` | string |  |
| `result[].multiAccountLoginCode` | number |  |
| `result[].newPasswordNeeded` | number |  |
| `result[].newPasswordToken` | string |  |
| `result[].password` | string |  |
| `result[].phone` | string |  |
| `result[].photo` | string |  |
| `result[].pushToken` | string |  |
| `result[].schoolId` | string |  |
| `result[].signatureId` | string |  |
| `result[].studentFollowerId` | array<string> |  |
| `result[].tags` | array<string> |  |
| `result[].trainingName` | string |  |
| `result[].username` | string |  |
| `result[].variables` | array<object> |  |
| `result[].variables[].name` | string |  |
| `result[].variables[].value` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Edusign API, this operation is `GET /v1/student` (base URL `https://ext.edusign.fr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-students.md) for the provider-specific parameters and requirements.

