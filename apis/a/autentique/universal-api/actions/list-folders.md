# Autentique: List Folders

Retrieves a list of folders from Autentique.

```
GET https://connect.mindcloud.co/v1/universal/autentique/latest/actions/list-folders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Autentique `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/autentique/latest/actions/list-folders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/autentique/latest/actions/list-folders?${params}`, {
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
      "childrenCounter": 1,
      "context": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "path": "string",
      "slug": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `childrenCounter` | number |  |
| `context` | string |  |
| `createdAt` | date |  |
| `id` | string |  |
| `name` | string |  |
| `path` | string |  |
| `slug` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Autentique API, this operation is `POST` (base URL `https://api.autentique.com.br/v2/graphql`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-folders.md) for the provider-specific parameters and requirements.

