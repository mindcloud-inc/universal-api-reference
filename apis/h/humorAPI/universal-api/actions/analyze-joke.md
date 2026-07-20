# Humor API: Analyze Joke



```
GET https://connect.mindcloud.co/v1/universal/humorAPI/latest/actions/analyze-joke
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Humor API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/humorAPI/latest/actions/analyze-joke?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/humorAPI/latest/actions/analyze-joke?${params}`, {
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
| `jokeText` | string | no | The joke text to analyze. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "joke": "string",
      "tags": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `joke` | string |  |
| `tags` | array<string> |  |

## Native endpoint

Through the native Humor API API, this operation is `POST /jokes/analyze` (base URL `https://api.humorapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/analyze-joke.md) for the provider-specific parameters and requirements.

