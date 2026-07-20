# Localazy: Translate With AI

Creates AI translations for source strings in Localazy.

```
POST https://connect.mindcloud.co/v1/universal/localazy/latest/actions/translate-with-ai
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Localazy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/localazy/latest/actions/translate-with-ai" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "from": "string",
  "to": "string",
  "items[]": [
    {}
  ],
  "items[].source": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/localazy/latest/actions/translate-with-ai', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "from": "string",
    "to": "string",
    "items[]": [{}],
    "items[].source": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | Localazy project identifier or slug. |
| `from` | string | yes | Source locale code. |
| `to` | string | yes | Target locale code. |
| `items[]` | array<object> | yes | Translation items to submit. |
| `items[].key` | string | no | Optional localization key. |
| `items[].source` | string | yes | Source text to translate. |
| `items[].comment` | string | no | Optional translation context. |
| `items[].lengthLimit` | number | no | Maximum translation length in characters. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fallback` | string | no | Fallback machine translation engine. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {}
      ],
      "message": "string",
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> | Translated items returned by Localazy AI. |
| `message` | string | Error message when the translation request fails. |
| `result` | boolean | Whether the translation request succeeded. |

## Native endpoint

Through the native Localazy API, this operation is `POST /projects/:projectId/ai` (base URL `https://api.localazy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/translate-with-ai.md) for the provider-specific parameters and requirements.

