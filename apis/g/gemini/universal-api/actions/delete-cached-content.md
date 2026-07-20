# Gemini: Delete Cached Content

Deletes a cached content resource from Gemini.

```
DELETE https://connect.mindcloud.co/v1/universal/gemini/latest/actions/delete-cached-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gemini `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/gemini/latest/actions/delete-cached-content?connectionId=$CONNECTION_ID&cachedContentId=w4i6kbw9vhe4uwdhammcobg657xjz3z5ode0lzks" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cachedContentId": "w4i6kbw9vhe4uwdhammcobg657xjz3z5ode0lzks"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gemini/latest/actions/delete-cached-content?${params}`, {
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
      "value": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | object | Empty object returned by Gemini when cached content is deleted successfully. |

## Native endpoint

Through the native Gemini API, this operation is `DELETE v1beta/cachedContents/:cachedContentId` (base URL `https://generativelanguage.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-cached-content.md) for the provider-specific parameters and requirements.

