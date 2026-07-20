# Google AI Studio: List Cached Contents

Retrieves cached content entries from Google AI Studio.

```
GET https://connect.mindcloud.co/v1/universal/googleAIStudio/latest/actions/list-cached-contents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google AI Studio `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleAIStudio/latest/actions/list-cached-contents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleAIStudio/latest/actions/list-cached-contents?${params}`, {
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
      "createTime": "2026-05-07T12:00:00.000Z",
      "displayName": "Ava Chen",
      "expireTime": "2026-05-07T12:00:00.000Z",
      "model": "string",
      "name": "Ava Chen",
      "updateTime": "2026-05-07T12:00:00.000Z",
      "usageMetadata": {
        "totalTokenCount": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createTime` | date | Cache creation timestamp. |
| `displayName` | string | User-provided cache display name. |
| `expireTime` | date | Cache expiration timestamp. |
| `model` | string | Model used by the cached content. |
| `name` | string | Cached content resource name. |
| `updateTime` | date | Last update timestamp. |
| `usageMetadata.totalTokenCount` | number | Total token count stored in the cache. |

## Native endpoint

Through the native Google AI Studio API, this operation is `GET v1beta/cachedContents` (base URL `https://generativelanguage.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-cached-contents.md) for the provider-specific parameters and requirements.

