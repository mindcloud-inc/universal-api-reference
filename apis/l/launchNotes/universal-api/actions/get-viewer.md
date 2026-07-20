# LaunchNotes: Get Viewer



```
GET https://connect.mindcloud.co/v1/universal/launchNotes/latest/actions/get-viewer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LaunchNotes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launchNotes/latest/actions/get-viewer?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launchNotes/latest/actions/get-viewer?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Viewer creation timestamp. |
| `email` | string | Viewer email address. |
| `id` | string | Viewer identifier. |
| `name` | string | Viewer display name. |
| `updatedAt` | date | Viewer update timestamp. |

## Native endpoint

Through the native LaunchNotes API, this operation is `POST /graphql` (base URL `https://app.launchnotes.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-viewer.md) for the provider-specific parameters and requirements.

