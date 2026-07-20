# Humor API: Get Random Joke



```
GET https://connect.mindcloud.co/v1/universal/humorAPI/latest/actions/get-random-joke
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Humor API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/humorAPI/latest/actions/get-random-joke?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/humorAPI/latest/actions/get-random-joke?${params}`, {
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
| `includeTags` | string | no | Comma-separated tags the joke should include. |
| `excludeTags` | string | no | Comma-separated tags the joke must not include. |
| `minRating` | number | no | Minimum rating between 0 and 10. |
| `maxLength` | number | no | Maximum joke length in letters. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "joke": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `joke` | string |  |

## Native endpoint

Through the native Humor API API, this operation is `GET /jokes/random` (base URL `https://api.humorapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-random-joke.md) for the provider-specific parameters and requirements.

