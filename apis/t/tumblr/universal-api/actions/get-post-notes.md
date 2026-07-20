# Tumblr: Get Post Notes

Retrieves notes for a Tumblr post.

```
GET https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/get-post-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tumblr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/get-post-notes?connectionId=$CONNECTION_ID&blogIdentifier=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "blogIdentifier": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/get-post-notes?${params}`, {
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
| `blogIdentifier` | string | yes | Any blog identifier. |
| `id` | string | yes | The post ID to fetch notes for. |
| `mode` | list<string> | no | Response formatting mode for the returned notes. One of: `all`, `conversation`, `likes`, `reblogs_with_tags`, `rollup`. Default: `all`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `beforeTimestamp` | number | no | Fetch notes created before this Unix timestamp in seconds. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "canHideOrDeleteNotes": true,
      "canSubscribe": true,
      "conversationalNotificationsEnabled": true,
      "isSubscribed": true,
      "notes": [
        {
          "avatarShape": "string",
          "avatarUrl": {
            "size128": "https://example.com",
            "size64": "https://example.com"
          },
          "blogName": "Ava Chen",
          "blogUrl": "https://example.com",
          "blogUuid": "string",
          "followed": true,
          "timestamp": 1,
          "type": "string"
        }
      ],
      "totalNotes": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canHideOrDeleteNotes` | boolean |  |
| `canSubscribe` | boolean |  |
| `conversationalNotificationsEnabled` | boolean |  |
| `isSubscribed` | boolean |  |
| `notes[].avatarShape` | string |  |
| `notes[].avatarUrl.size128` | string |  |
| `notes[].avatarUrl.size64` | string |  |
| `notes[].blogName` | string |  |
| `notes[].blogUrl` | string |  |
| `notes[].blogUuid` | string |  |
| `notes[].followed` | boolean |  |
| `notes[].timestamp` | number |  |
| `notes[].type` | string |  |
| `totalNotes` | number |  |

## Native endpoint

Through the native Tumblr API, this operation is `GET /v2/blog/:blogIdentifier/notes` (base URL `https://api.tumblr.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-post-notes.md) for the provider-specific parameters and requirements.

