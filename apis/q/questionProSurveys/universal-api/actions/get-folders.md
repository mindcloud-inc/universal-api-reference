# QuestionPro Surveys: Get Folders



```
GET https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-folders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuestionPro Surveys `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-folders?connectionId=$CONNECTION_ID&limit=25&offset=0&userId=6358571" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "userId": "6358571"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-folders?${params}`, {
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
| `userId` | number | yes | The QuestionPro user ID. Example: `6358571`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creationDate": "string",
      "folderID": 1,
      "folderName": "Ava Chen",
      "isDefault": true,
      "surveyCount": 1,
      "userID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creationDate` | string |  |
| `folderID` | number |  |
| `folderName` | string |  |
| `isDefault` | boolean |  |
| `surveyCount` | number |  |
| `userID` | number |  |

## Native endpoint

Through the native QuestionPro Surveys API, this operation is `GET users/:userId/folders` (base URL `https://api.questionpro.com/a/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-folders.md) for the provider-specific parameters and requirements.

