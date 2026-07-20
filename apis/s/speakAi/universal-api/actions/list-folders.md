# Speak Ai: List Folders

Retrieves folders from Speak Ai.

```
GET https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/list-folders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Speak Ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/list-folders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/list-folders?${params}`, {
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
      "folders": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "description": "string",
          "folderId": "string",
          "name": "Ava Chen",
          "showOrder": 1,
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "user": {
            "firstName": "Ava",
            "lastName": "Chen",
            "picture": "string"
          },
          "userId": "string"
        }
      ],
      "pages": 1,
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `folders[].createdAt` | date |  |
| `folders[].description` | string |  |
| `folders[].folderId` | string |  |
| `folders[].name` | string |  |
| `folders[].showOrder` | number |  |
| `folders[].updatedAt` | date |  |
| `folders[].user.firstName` | string |  |
| `folders[].user.lastName` | string |  |
| `folders[].user.picture` | string |  |
| `folders[].userId` | string |  |
| `pages` | number |  |
| `totalCount` | number |  |

## Native endpoint

Through the native Speak Ai API, this operation is `GET /folder` (base URL `https://api.speakai.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-folders.md) for the provider-specific parameters and requirements.

