# MetaSurvey: List Folders



```
GET https://connect.mindcloud.co/v1/universal/metaSurvey/latest/actions/list-folders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MetaSurvey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/metaSurvey/latest/actions/list-folders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/metaSurvey/latest/actions/list-folders?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "hasNewData": true,
      "name": "Ava Chen",
      "permission": "string",
      "surveysCount": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | MetaSurvey folder identifier. |
| `createdAt` | date | When the folder was created. |
| `hasNewData` | boolean | Whether the folder contains new survey response data. |
| `name` | string | Folder name. |
| `permission` | string | Current user permission for the folder. |
| `surveysCount` | number | Number of surveys in the folder. |
| `updatedAt` | date | When the folder was last updated. |
| `userId` | string | Folder owner user identifier. |

## Native endpoint

Through the native MetaSurvey API, this operation is `GET /admin/folders` (base URL `https://api.getmetasurvey.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-folders.md) for the provider-specific parameters and requirements.

