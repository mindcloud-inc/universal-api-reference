# Gemini: Update Cached Content

Updates a cached content resource in Gemini.

```
PUT https://connect.mindcloud.co/v1/universal/gemini/latest/actions/update-cached-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gemini `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/gemini/latest/actions/update-cached-content" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cachedContentId": "w4i6kbw9vhe4uwdhammcobg657xjz3z5ode0lzks",
  "updateMask": "ttl",
  "ttl": "7200s"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gemini/latest/actions/update-cached-content', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cachedContentId": "w4i6kbw9vhe4uwdhammcobg657xjz3z5ode0lzks",
    "updateMask": "ttl",
    "ttl": "7200s"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cachedContentId` | string | yes | Cached content ID segment (without `cachedContents/` prefix). Example: `w4i6kbw9vhe4uwdhammcobg657xjz3z5ode0lzks`. |
| `updateMask` | string | yes | Comma-separated fields to update. Use `ttl` for TTL-only updates. Default: `ttl`. Example: `ttl`. |
| `ttl` | string | yes | New cache TTL duration, e.g. `7200s`. Example: `7200s`. |

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

Through the native Gemini API, this operation is `PATCH v1beta/cachedContents/:cachedContentId` (base URL `https://generativelanguage.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-cached-content.md) for the provider-specific parameters and requirements.

