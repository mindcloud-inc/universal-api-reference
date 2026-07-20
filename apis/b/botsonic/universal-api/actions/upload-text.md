# Botsonic: Upload Text

Uploads text as bot data in Botsonic.

```
POST https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/upload-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Botsonic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/upload-text" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "data_123",
  "botId": "bot_123",
  "text": "This text will be used to train the bot."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/upload-text', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "data_123",
    "botId": "bot_123",
    "text": "This text will be used to train the bot."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Upload identifier. Example: `data_123`. |
| `botId` | string | yes | Bot identifier. Example: `bot_123`. |
| `text` | string | yes | Training text to upload. Example: `This text will be used to train the bot.`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | no | Optional title for the uploaded text. Example: `Product documentation`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Botsonic API returns.

## Native endpoint

Through the native Botsonic API, this operation is `POST /v1/business/bot-data/upload-text` (base URL `https://api.botsonic.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-text.md) for the provider-specific parameters and requirements.

