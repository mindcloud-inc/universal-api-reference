# WordsAPI: Get Member Of

Retrieves groups that a word belongs to from WordsAPI.

```
GET https://connect.mindcloud.co/v1/universal/wordsAPI/latest/actions/get-member-of
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WordsAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wordsAPI/latest/actions/get-member-of?connectionId=$CONNECTION_ID&word=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "word": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wordsAPI/latest/actions/get-member-of?${params}`, {
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
| `word` | string | yes | The word to retrieve from WordsAPI. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native WordsAPI API returns.

## Native endpoint

Through the native WordsAPI API, this operation is `GET /words/{word}/memberOf` (base URL `https://wordsapiv1.p.rapidapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-member-of.md) for the provider-specific parameters and requirements.

