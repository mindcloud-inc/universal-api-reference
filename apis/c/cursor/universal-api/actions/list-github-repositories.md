# Cursor: List GitHub Repositories



```
GET https://connect.mindcloud.co/v1/universal/cursor/latest/actions/list-github-repositories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cursor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cursor/latest/actions/list-github-repositories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cursor/latest/actions/list-github-repositories?${params}`, {
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
      "name": "Ava Chen",
      "owner": "string",
      "repository": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string | Repository name. |
| `owner` | string | Repository owner. |
| `repository` | string | Full GitHub repository URL. |

## Native endpoint

Through the native Cursor API, this operation is `GET /v0/repositories` (base URL `https://api.cursor.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-github-repositories.md) for the provider-specific parameters and requirements.

