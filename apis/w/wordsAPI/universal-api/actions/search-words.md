# WordsAPI: Search Words

Finds words in WordsAPI by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/wordsAPI/latest/actions/search-words
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WordsAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wordsAPI/latest/actions/search-words?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wordsAPI/latest/actions/search-words?${params}`, {
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
| `hasDetails` | string | no | Return only words that contain a specific detail type. |
| `letterPattern` | string | no | Regex-like pattern to match words. |
| `partOfSpeech` | string | no | Restrict results by part of speech. |
| `soundsMax` | string | no | Maximum number of sounds. |
| `soundsMin` | string | no | Minimum number of sounds. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native WordsAPI API returns.

## Native endpoint

Through the native WordsAPI API, this operation is `GET /words` (base URL `https://wordsapiv1.p.rapidapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-words.md) for the provider-specific parameters and requirements.

