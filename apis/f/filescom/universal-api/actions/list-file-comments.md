# Files.com: List File Comments

Retrieves file comments by path from Files.com.

```
GET https://connect.mindcloud.co/v1/universal/filescom/latest/actions/list-file-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Files.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/filescom/latest/actions/list-file-comments?connectionId=$CONNECTION_ID&path=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "path": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/filescom/latest/actions/list-file-comments?${params}`, {
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
| `path` | string | yes | File or folder path without leading or trailing slashes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": "string",
      "id": 1,
      "path": "string",
      "reactions": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string |  |
| `id` | number |  |
| `path` | string |  |
| `reactions` | array<object> |  |

## Native endpoint

Through the native Files.com API, this operation is `GET /file_comments/files/:path` (base URL `{{credentials.siteUrl}}/api/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-file-comments.md) for the provider-specific parameters and requirements.

