# ElevenLabs: Get History Item

Retrieves a generated audio item from ElevenLabs.

```
GET https://connect.mindcloud.co/v1/universal/elevenLabs/latest/actions/get-history-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ElevenLabs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/elevenLabs/latest/actions/get-history-item?connectionId=$CONNECTION_ID&historyItemId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "historyItemId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/elevenLabs/latest/actions/get-history-item?${params}`, {
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
| `historyItemId` | string | yes | The history item identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ElevenLabs API returns.

## Native endpoint

Through the native ElevenLabs API, this operation is `GET /history/:history_item_id` (base URL `https://api.elevenlabs.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-history-item.md) for the provider-specific parameters and requirements.

