# Hume AI: Create Config

Creates a new EVI config in Hume AI.

```
POST https://connect.mindcloud.co/v1/universal/humeAI/latest/actions/create-config
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hume AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/humeAI/latest/actions/create-config" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eviVersion": "3",
  "name": "Ava Chen",
  "voice.provider": "HUME_AI",
  "voice.name": "Ava Song"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/humeAI/latest/actions/create-config', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eviVersion": "3",
    "name": "Ava Chen",
    "voice.provider": "HUME_AI",
    "voice.name": "Ava Song"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `eviVersion` | string | yes | EVI version to use. Default: `3`. |
| `name` | string | yes | Config name. |
| `voice.provider` | string | yes | Voice provider for the config voice. Default: `HUME_AI`. |
| `voice.name` | string | yes | Voice name for the config voice. Default: `Ava Song`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "builtinTools": [
        {}
      ],
      "createdOn": 1,
      "ellmModel": {},
      "eventMessages": {},
      "eviVersion": "string",
      "id": "string",
      "languageModel": {},
      "modifiedOn": 1,
      "name": "Ava Chen",
      "nudges": {},
      "prompt": {},
      "timeouts": {},
      "tools": [
        {}
      ],
      "version": 1,
      "versionDescription": "string",
      "voice": {},
      "webhooks": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `builtinTools` | array<object> | Attached built-in tools. |
| `createdOn` | number | Creation timestamp in milliseconds. |
| `ellmModel` | object | ELLM model configuration. |
| `eventMessages` | object | Event message settings. |
| `eviVersion` | string | EVI version. |
| `id` | string | Config ID. |
| `languageModel` | object | Language model configuration. |
| `modifiedOn` | number | Last modification timestamp in milliseconds. |
| `name` | string | Config name. |
| `nudges` | object | Nudge settings. |
| `prompt` | object | Prompt configuration. |
| `timeouts` | object | Timeout settings. |
| `tools` | array<object> | Attached tools. |
| `version` | number | Config version number. |
| `versionDescription` | string | Optional version description. |
| `voice` | object | Voice configuration. |
| `webhooks` | array<object> | Webhook settings. |

## Native endpoint

Through the native Hume AI API, this operation is `POST /v0/evi/configs` (base URL `https://api.hume.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-config.md) for the provider-specific parameters and requirements.

