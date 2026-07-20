# Speak Ai: Get Folder

Retrieves folder details from Speak Ai.

```
GET https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/get-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Speak Ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/get-folder?connectionId=$CONNECTION_ID&folderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "folderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/get-folder?${params}`, {
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
| `folderId` | string | yes | Speak Ai folder identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "folderId": "string",
      "folderType": "string",
      "isDeleted": true,
      "name": "Ava Chen",
      "showOrder": 1,
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
| `companyId` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `folderId` | string |  |
| `folderType` | string |  |
| `isDeleted` | boolean |  |
| `name` | string |  |
| `showOrder` | number |  |
| `updatedAt` | date |  |
| `userId` | string |  |

## Native endpoint

Through the native Speak Ai API, this operation is `GET /folder/:folderId` (base URL `https://api.speakai.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-folder.md) for the provider-specific parameters and requirements.

