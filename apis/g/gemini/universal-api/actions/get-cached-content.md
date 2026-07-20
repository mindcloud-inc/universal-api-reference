# Gemini: Get Cached Content

Retrieves a cached content resource from Gemini.

```
GET https://connect.mindcloud.co/v1/universal/gemini/latest/actions/get-cached-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gemini `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gemini/latest/actions/get-cached-content?connectionId=$CONNECTION_ID&cachedContentId=w4i6kbw9vhe4uwdhammcobg657xjz3z5ode0lzks" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cachedContentId": "w4i6kbw9vhe4uwdhammcobg657xjz3z5ode0lzks"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gemini/latest/actions/get-cached-content?${params}`, {
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
| `cachedContentId` | string | yes | Cached content ID segment (without `cachedContents/` prefix). Example: `w4i6kbw9vhe4uwdhammcobg657xjz3z5ode0lzks`. |

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

Through the native Gemini API, this operation is `GET v1beta/cachedContents/:cachedContentId` (base URL `https://generativelanguage.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-cached-content.md) for the provider-specific parameters and requirements.

