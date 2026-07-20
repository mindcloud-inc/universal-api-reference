# Google AI Studio: Delete Cached Content

Deletes a cached content entry from Google AI Studio.

```
DELETE https://connect.mindcloud.co/v1/universal/googleAIStudio/latest/actions/delete-cached-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google AI Studio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/googleAIStudio/latest/actions/delete-cached-content?connectionId=$CONNECTION_ID&cachedContentId=cachedContents%2Fabc123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cachedContentId": "cachedContents/abc123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleAIStudio/latest/actions/delete-cached-content?${params}`, {
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
| `cachedContentId` | string | yes | Full cached content resource name, for example `cachedContents/abc123`. Example: `cachedContents/abc123`. |

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

Through the native Google AI Studio API, this operation is `DELETE v1beta/cachedContents/:cachedContentId` (base URL `https://generativelanguage.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-cached-content.md) for the provider-specific parameters and requirements.

