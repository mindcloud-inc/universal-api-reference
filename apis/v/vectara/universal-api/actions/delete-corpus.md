# Vectara: Delete Corpus

Deletes an existing corpus from Vectara.

```
DELETE https://connect.mindcloud.co/v1/universal/vectara/latest/actions/delete-corpus
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vectara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/vectara/latest/actions/delete-corpus?connectionId=$CONNECTION_ID&corpusKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "corpusKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vectara/latest/actions/delete-corpus?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `corpusKey` | string | yes | Unique key of the corpus. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Vectara API returns.

## Native endpoint

Through the native Vectara API, this operation is `DELETE /v2/corpora/:corpus_key` (base URL `https://api.vectara.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-corpus.md) for the provider-specific parameters and requirements.

