# lobst.rs: Get Comment

Retrieves a comment from lobst.rs.

```
GET https://connect.mindcloud.co/v1/universal/lobstrs/latest/actions/get-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a lobst.rs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lobstrs/latest/actions/get-comment?connectionId=$CONNECTION_ID&commentShortId=efgamd" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "commentShortId": "efgamd"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lobstrs/latest/actions/get-comment?${params}`, {
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
| `commentShortId` | string | yes | Lobsters comment short ID, such as efgamd. Example: `efgamd`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": "string",
      "comment_plain": "string",
      "commenting_user": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "depth": 1,
      "flags": 1,
      "is_deleted": true,
      "is_moderated": true,
      "last_edited_at": "2026-05-07T12:00:00.000Z",
      "score": 1,
      "short_id": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | string |  |
| `comment_plain` | string |  |
| `commenting_user` | string |  |
| `created_at` | date |  |
| `depth` | number |  |
| `flags` | number |  |
| `is_deleted` | boolean |  |
| `is_moderated` | boolean |  |
| `last_edited_at` | date |  |
| `score` | number |  |
| `short_id` | string |  |
| `url` | string |  |

## Native endpoint

Through the native lobst.rs API, this operation is `GET /c/:commentShortId.json` (base URL `https://lobste.rs`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-comment.md) for the provider-specific parameters and requirements.

