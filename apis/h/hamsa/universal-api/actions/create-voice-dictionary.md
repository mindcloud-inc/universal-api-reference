# Hamsa: Create Voice Dictionary

Creates a new voice dictionary in Hamsa.

```
POST https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/create-voice-dictionary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hamsa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/create-voice-dictionary" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "words[]": [
    {}
  ],
  "words[].pronunciation": "string",
  "words[].word": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/create-voice-dictionary', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "words[]": [{}],
    "words[].pronunciation": "string",
    "words[].pronunciation": "string",
    "words[].word": "string",
    "words[].word": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `words[]` | array<object> | yes |  |
| `words[].pronunciation` | string | yes |  |
| `words[].pronunciation` | string | yes |  |
| `words[].word` | string | yes |  |
| `words[].word` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "words": [
        {
          "pronunciation": "string",
          "word": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `id` | string |  |
| `name` | string |  |
| `words[].pronunciation` | string |  |
| `words[].word` | string |  |

## Native endpoint

Through the native Hamsa API, this operation is `POST /v1/voice-agents/voice-dictionaries` (base URL `https://api.tryhamsa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-voice-dictionary.md) for the provider-specific parameters and requirements.

