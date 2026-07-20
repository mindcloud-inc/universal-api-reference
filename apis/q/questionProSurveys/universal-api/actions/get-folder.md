# QuestionPro Surveys: Get Folder



```
GET https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuestionPro Surveys `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-folder?connectionId=$CONNECTION_ID&userId=6358571&folderId=6773259" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "6358571",
  "folderId": "6773259"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-folder?${params}`, {
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
| `folderId` | number | yes | The QuestionPro folder ID. Example: `6773259`. |

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
| `creationDate` | string | The folder creation date. |
| `folderID` | number | The QuestionPro folder ID. |
| `folderName` | string | The folder name. |
| `isDefault` | boolean | Whether this is the default folder. |
| `surveyCount` | number | The number of surveys in the folder. |
| `userID` | number | The QuestionPro user ID that owns the folder. |

## Native endpoint

Through the native QuestionPro Surveys API, this operation is `GET users/:userId/folders/:folderId` (base URL `https://api.questionpro.com/a/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-folder.md) for the provider-specific parameters and requirements.

