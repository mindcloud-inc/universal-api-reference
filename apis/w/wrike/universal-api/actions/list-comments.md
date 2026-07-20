# Wrike: List Comments

Finds comments in Wrike.

```
GET https://connect.mindcloud.co/v1/universal/wrike/latest/actions/list-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wrike `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wrike/latest/actions/list-comments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wrike/latest/actions/list-comments?${params}`, {
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
      "createdDate": "2026-05-07T12:00:00.000Z",
      "direction": "string",
      "emailSubject": "ava@example.com",
      "folderId": "string",
      "id": "string",
      "taskId": "string",
      "text": "string",
      "type": "string",
      "updatedDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authorId` | string |  |
| `createdDate` | date |  |
| `direction` | string |  |
| `emailSubject` | string |  |
| `folderId` | string |  |
| `id` | string |  |
| `taskId` | string |  |
| `text` | string |  |
| `type` | string |  |
| `updatedDate` | date |  |

## Native endpoint

Through the native Wrike API, this operation is `GET /comments` (base URL `https://{{credentials.accessTokenRequest.host}}/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-comments.md) for the provider-specific parameters and requirements.

