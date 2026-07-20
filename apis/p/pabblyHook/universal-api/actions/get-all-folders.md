# Pabbly Hook: Get All Folders



```
GET https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/get-all-folders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Hook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/get-all-folders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/get-all-folders?${params}`, {
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
      "connectionCount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "Id": "string",
      "name": "Ava Chen",
      "sortOrder": 1,
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
| `connectionCount` | number | Number of connections in the folder. |
| `createdAt` | date | Folder creation timestamp. |
| `Id` | string | Pabbly Hook folder identifier. |
| `name` | string | Folder name. |
| `sortOrder` | number | Folder sort order. |
| `updatedAt` | date | Folder update timestamp. |
| `userId` | string | Pabbly account user identifier that owns the folder. |

## Native endpoint

Through the native Pabbly Hook API, this operation is `GET /api/v1/folders` (base URL `https://hook.pabbly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-folders.md) for the provider-specific parameters and requirements.

