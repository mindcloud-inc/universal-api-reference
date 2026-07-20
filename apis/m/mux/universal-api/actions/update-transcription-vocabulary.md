# Mux: Update Transcription Vocabulary



```
PUT https://connect.mindcloud.co/v1/universal/mux/latest/actions/update-transcription-vocabulary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mux `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mux/latest/actions/update-transcription-vocabulary" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "phrases[]": [
    "string"
  ],
  "transcriptionVocabularyId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mux/latest/actions/update-transcription-vocabulary', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "phrases[]": ["string"],
    "transcriptionVocabularyId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `phrases[]` | array<string> | yes | The phrase list for the vocabulary. |
| `transcriptionVocabularyId` | string | yes | The transcription vocabulary ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |

## Native endpoint

Through the native Mux API, this operation is `PUT /video/v1/transcription-vocabularies/{TRANSCRIPTION_VOCABULARY_ID}` (base URL `https://api.mux.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-transcription-vocabulary.md) for the provider-specific parameters and requirements.

