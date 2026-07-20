# WordsAPI: Get Random Word

Retrieves a random word from WordsAPI.

```
GET https://connect.mindcloud.co/v1/universal/wordsAPI/latest/actions/get-random-word
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WordsAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wordsAPI/latest/actions/get-random-word?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wordsAPI/latest/actions/get-random-word?${params}`, {
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
| `random` | string | no | Return one random word. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native WordsAPI API returns.

## Native endpoint

Through the native WordsAPI API, this operation is `GET /words` (base URL `https://wordsapiv1.p.rapidapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-random-word.md) for the provider-specific parameters and requirements.

