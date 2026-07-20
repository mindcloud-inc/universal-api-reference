# ElevenLabs: List Generated Items

Retrieves previously generated audio from ElevenLabs.

```
GET https://connect.mindcloud.co/v1/universal/elevenLabs/latest/actions/list-generated-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ElevenLabs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/elevenLabs/latest/actions/list-generated-items?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/elevenLabs/latest/actions/list-generated-items?${params}`, {
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
| `pageSize` | number | no |  |
| `startAfterHistoryItemId` | string | no |  |
| `voiceId` | string | no |  |
| `modelId` | string | no |  |
| `dateBeforeUnix` | number | no |  |
| `dateAfterUnix` | number | no |  |
| `sortDirection` | string | no |  |
| `search` | string | no |  |
| `source` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ElevenLabs API returns.

## Native endpoint

Through the native ElevenLabs API, this operation is `GET /history` (base URL `https://api.elevenlabs.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-generated-items.md) for the provider-specific parameters and requirements.

