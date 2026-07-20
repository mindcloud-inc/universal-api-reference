# Hamsa: Update Voice Dictionary

Updates an existing voice dictionary in Hamsa.

```
PUT https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/update-voice-dictionary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hamsa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/update-voice-dictionary" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "name": "Ava Chen",
  "words[]": [
    {}
  ],
  "words[].pronunciation": "string",
  "words[].word": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/update-voice-dictionary', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
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
| `id` | string | yes |  |
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
      "id": "string",
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z",
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
| `id` | string |  |
| `name` | string |  |
| `updatedAt` | date |  |
| `words[].pronunciation` | string |  |
| `words[].word` | string |  |

## Native endpoint

Through the native Hamsa API, this operation is `PATCH /v1/voice-agents/voice-dictionaries/:voiceDictionaryId` (base URL `https://api.tryhamsa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-voice-dictionary.md) for the provider-specific parameters and requirements.

