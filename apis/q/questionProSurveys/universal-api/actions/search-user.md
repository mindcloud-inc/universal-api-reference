# QuestionPro Surveys: Search User



```
GET https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/search-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuestionPro Surveys `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/search-user?connectionId=$CONNECTION_ID&organizationId=6137544&emailAddress=apps%40mindcloud.co" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "6137544",
  "emailAddress": "apps@mindcloud.co"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/search-user?${params}`, {
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
| `emailAddress` | string | yes | The email address to search for. Example: `apps@mindcloud.co`. |

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
| `creationDate` | string | The user creation date. |
| `departmentID` | number | The QuestionPro department ID. |
| `emailAddress` | string | The user's email address. |
| `firstName` | string | The user's first name. |
| `lastName` | string | The user's last name. |
| `licenseStartDate` | string | The license start date. |
| `licenseType` | string | The QuestionPro license type. |
| `organizationID` | number | The QuestionPro organization ID. |
| `phone` | string | The user's phone number. |
| `userID` | number | The QuestionPro user ID. |
| `userType` | string | The user type. |

## Native endpoint

Through the native QuestionPro Surveys API, this operation is `GET organizations/:organizationId/users/search` (base URL `https://api.questionpro.com/a/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-user.md) for the provider-specific parameters and requirements.

