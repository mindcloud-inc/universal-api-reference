# Wrike: List Attachments

Finds attachments in Wrike.

```
GET https://connect.mindcloud.co/v1/universal/wrike/latest/actions/list-attachments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wrike `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wrike/latest/actions/list-attachments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wrike/latest/actions/list-attachments?${params}`, {
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
      "authorId": "string",
      "commentId": "string",
      "contentType": "string",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "folderId": "string",
      "height": 1,
      "id": "string",
      "name": "Ava Chen",
      "playlistUrl": "https://example.com",
      "previewUrl": "https://example.com",
      "size": 1,
      "taskId": "string",
      "type": "string",
      "url": "https://example.com",
      "version": 1,
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authorId` | string |  |
| `commentId` | string |  |
| `contentType` | string |  |
| `createdDate` | date |  |
| `folderId` | string |  |
| `height` | number |  |
| `id` | string |  |
| `name` | string |  |
| `playlistUrl` | string |  |
| `previewUrl` | string |  |
| `size` | number |  |
| `taskId` | string |  |
| `type` | string |  |
| `url` | string |  |
| `version` | number |  |
| `width` | number |  |

## Native endpoint

Through the native Wrike API, this operation is `GET /attachments` (base URL `https://{{credentials.accessTokenRequest.host}}/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-attachments.md) for the provider-specific parameters and requirements.

