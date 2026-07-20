# QuestionPro Surveys: Get All Users from Organization



```
GET https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-all-users-from-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuestionPro Surveys `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-all-users-from-organization?connectionId=$CONNECTION_ID&limit=25&offset=0&organizationId=6137544" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organizationId": "6137544"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-all-users-from-organization?${params}`, {
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
| `organizationId` | number | yes | The QuestionPro organization ID. Example: `6137544`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creationDate": "string",
      "departmentID": 1,
      "emailAddress": "ava@example.com",
      "firstName": "Ava",
      "lastName": "Chen",
      "licenseStartDate": "string",
      "licenseType": "string",
      "organizationID": 1,
      "phone": "string",
      "userID": 1,
      "userType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creationDate` | string |  |
| `departmentID` | number |  |
| `emailAddress` | string |  |
| `firstName` | string |  |
| `lastName` | string |  |
| `licenseStartDate` | string |  |
| `licenseType` | string |  |
| `organizationID` | number |  |
| `phone` | string |  |
| `userID` | number |  |
| `userType` | string |  |

## Native endpoint

Through the native QuestionPro Surveys API, this operation is `GET organizations/:organizationId/users` (base URL `https://api.questionpro.com/a/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-all-users-from-organization.md) for the provider-specific parameters and requirements.

