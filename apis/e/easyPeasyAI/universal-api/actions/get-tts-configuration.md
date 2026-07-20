# Easy-Peasy.AI: Get TTS Configuration

Retrieves TTS voice configuration from Easy-Peasy.AI.

```
GET https://connect.mindcloud.co/v1/universal/easyPeasyAI/latest/actions/get-tts-configuration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easy-Peasy.AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyPeasyAI/latest/actions/get-tts-configuration?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyPeasyAI/latest/actions/get-tts-configuration?${params}`, {
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
| `language` | string | no | Optional language code used to scope TTS configuration. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Easy-Peasy.AI API returns.

## Native endpoint

Through the native Easy-Peasy.AI API, this operation is `GET /api/get-text-to-speech-config` (base URL `https://easy-peasy.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tts-configuration.md) for the provider-specific parameters and requirements.

