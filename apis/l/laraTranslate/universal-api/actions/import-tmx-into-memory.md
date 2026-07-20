# Lara Translate: Import TMX into memory

Imports a TMX file into a Lara Translate memory.

```
POST https://connect.mindcloud.co/v1/universal/laraTranslate/latest/actions/import-tmx-into-memory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lara Translate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/laraTranslate/latest/actions/import-tmx-into-memory" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "mem_123",
  "tmx_content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/laraTranslate/latest/actions/import-tmx-into-memory', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "mem_123",
    "tmx_content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | ID of the translation memory to import TMX content into. Example: `mem_123`. |
| `tmx_content` | string | yes | Raw TMX file content. |

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
| `id` | string |  |
| `progress` | number |  |
| `size` | number |  |

## Native endpoint

Through the native Lara Translate API, this operation is `POST /` (base URL `https://mcp-v2.laratranslate.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-tmx-into-memory.md) for the provider-specific parameters and requirements.

