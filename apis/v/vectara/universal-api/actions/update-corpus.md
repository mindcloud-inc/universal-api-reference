# Vectara: Update Corpus

Updates an existing corpus in Vectara.

```
PUT https://connect.mindcloud.co/v1/universal/vectara/latest/actions/update-corpus
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vectara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/vectara/latest/actions/update-corpus" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "corpusKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vectara/latest/actions/update-corpus', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "corpusKey": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `corpusKey` | string | yes | Unique key of the corpus. |
| `enabled` | boolean | no | Whether the corpus is enabled. |
| `name` | string | no | Updated corpus name. |
| `description` | string | no | Updated corpus description. |
| `saveHistory` | boolean | no | Whether this corpus should save query history by default. |

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

Through the native Vectara API, this operation is `PATCH /v2/corpora/:corpus_key` (base URL `https://api.vectara.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-corpus.md) for the provider-specific parameters and requirements.

