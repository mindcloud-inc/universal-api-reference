# Lara Translate: Add translation unit to memory

Adds a translation unit to a Lara Translate memory.

```
POST https://connect.mindcloud.co/v1/universal/laraTranslate/latest/actions/add-translation-unit-to-memory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lara Translate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/laraTranslate/latest/actions/add-translation-unit-to-memory" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "mem_123",
  "source": "en-US",
  "target": "it-IT",
  "sentence": "string",
  "translation": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/laraTranslate/latest/actions/add-translation-unit-to-memory', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "mem_123",
    "source": "en-US",
    "target": "it-IT",
    "sentence": "string",
    "translation": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string<string> | yes | The translation memory ID to receive the translation unit. Example: `mem_123`. |
| `source` | string | yes | Source language code for the sentence. Example: `en-US`. |
| `target` | string | yes | Target language code for the translation. Example: `it-IT`. |
| `sentence` | string | yes | Source sentence. |
| `translation` | string | yes | Translated sentence. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tuid` | string | no | Optional translation unit identifier. |
| `sentence_before` | string | no | Optional sentence before the source sentence for context. |
| `sentence_after` | string | no | Optional sentence after the source sentence for context. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "begin": 1,
      "channel": 1,
      "end": 1,
      "id": "string",
      "progress": 1,
      "size": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `begin` | number |  |
| `channel` | number |  |
| `end` | number |  |
| `id` | string | Import job ID. |
| `progress` | number |  |
| `size` | number |  |

## Native endpoint

Through the native Lara Translate API, this operation is `POST /` (base URL `https://mcp-v2.laratranslate.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-translation-unit-to-memory.md) for the provider-specific parameters and requirements.

