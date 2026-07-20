# Vectara: Create Corpus

Creates a new corpus in Vectara.

```
POST https://connect.mindcloud.co/v1/universal/vectara/latest/actions/create-corpus
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vectara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vectara/latest/actions/create-corpus" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "key": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vectara/latest/actions/create-corpus', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "key": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `key` | string | yes | Unique key for the new corpus. |
| `name` | string | no | Display name for the corpus. |
| `description` | string | no | Description of the corpus. |
| `saveHistory` | boolean | no | Whether queries to this corpus should be saved by default. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `queriesAreAnswers` | boolean | no | Treat queries as answers instead of questions. |
| `documentsAreQuestions` | boolean | no | Treat indexed documents as questions instead of answers. |
| `encoderName` | string | no | Encoder name to use for the corpus. |
| `filterAttributes[]` | array<object> | no | Filter attribute definitions for the corpus. |
| `customDimensions[]` | array<object> | no | Custom dimension definitions for the corpus. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chat_history_corpus": true,
      "created_at": "2026-05-07T12:00:00.000Z",
      "custom_dimensions": [
        {}
      ],
      "description": "string",
      "documents_are_questions": true,
      "enabled": true,
      "encoder_id": "string",
      "encoder_name": "Ava Chen",
      "filter_attributes": [
        {}
      ],
      "id": "string",
      "key": "string",
      "limits": {},
      "name": "Ava Chen",
      "queries_are_answers": true,
      "save_history": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chat_history_corpus` | boolean | Whether this corpus stores chats instead of documents. |
| `created_at` | date | When the corpus was created. |
| `custom_dimensions` | array<object> | Custom dimensions configured on the corpus. |
| `description` | string | Corpus description. |
| `documents_are_questions` | boolean | Whether documents in this corpus are treated as questions. |
| `enabled` | boolean | Whether the corpus is enabled. |
| `encoder_id` | string | Deprecated encoder ID. |
| `encoder_name` | string | Encoder used by the corpus. |
| `filter_attributes` | array<object> | Filter attributes configured on the corpus. |
| `id` | string | Vectara ID of the corpus. |
| `key` | string | A user-provided key for a corpus. |
| `limits` | object | Usage and limit information for the corpus. |
| `name` | string | Name for the corpus. |
| `queries_are_answers` | boolean | Whether queries to this corpus are treated as answers. |
| `save_history` | boolean | Whether queries are saved to history by default. |

## Native endpoint

Through the native Vectara API, this operation is `POST /v2/corpora` (base URL `https://api.vectara.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-corpus.md) for the provider-specific parameters and requirements.

