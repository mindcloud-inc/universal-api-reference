# Edusign: List Students by IDs

Retrieves students from Edusign by ID list.

```
GET https://connect.mindcloud.co/v1/universal/edusign/latest/actions/list-students-by-ids
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Edusign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/edusign/latest/actions/list-students-by-ids?connectionId=$CONNECTION_ID&studentIds%5B%5D=string&studentIds%5B%5D=string&studentIds%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "studentIds[]": "string",
  "studentIds[]": "string",
  "studentIds[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/edusign/latest/actions/list-students-by-ids?${params}`, {
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
| `studentIds[]` | array<string> | yes |  |
| `studentIds[]` | array<string> | yes |  |
| `studentIds[]` | array<string> | yes |  |

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
            "string"
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
| `result[].groups` | array<string> |  |
| `result[].hidden` | number |  |
| `result[].id` | string |  |
| `result[].language` | string |  |
| `result[].lastname` | string |  |
| `result[].multiAccountLoginCode` | number |  |
| `result[].newPasswordNeeded` | number |  |
| `result[].phone` | string |  |
| `result[].photo` | string |  |
| `result[].schoolId` | string |  |
| `result[].signatureId` | string |  |
| `result[].studentFollowerId` | array<string> |  |
| `result[].tags` | array<string> |  |
| `result[].trainingIds` | array<string> |  |
| `result[].trainingName` | string |  |
| `result[].username` | string |  |
| `result[].variables` | array<string> |  |
| `status` | string |  |

## Native endpoint

Through the native Edusign API, this operation is `POST /v1/student/by-ids` (base URL `https://ext.edusign.fr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-students-by-ids.md) for the provider-specific parameters and requirements.

