# Documo: List Cover Pages

Retrieves cover page templates from Documo.

```
GET https://connect.mindcloud.co/v1/universal/documo/latest/actions/list-cover-pages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documo/latest/actions/list-cover-pages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documo/latest/actions/list-cover-pages?${params}`, {
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
      "accountId": "string",
      "file": {
        "id": "string",
        "mimeType": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "fileId": "string",
      "id": "string",
      "isPublic": true,
      "name": "Ava Chen",
      "previewLink": "https://example.com",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `file.id` | string |  |
| `file.mimeType` | string |  |
| `file.name` | string |  |
| `file.type` | string |  |
| `fileId` | string |  |
| `id` | string |  |
| `isPublic` | boolean |  |
| `name` | string |  |
| `previewLink` | string |  |
| `updatedAt` | date |  |
| `userId` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Documo API, this operation is `GET /coverpages` (base URL `https://api.documo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-cover-pages.md) for the provider-specific parameters and requirements.

