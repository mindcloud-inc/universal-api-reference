# Official Joke API: Get Ten Jokes by Type



```
GET https://connect.mindcloud.co/v1/universal/officialJokeAPI/latest/actions/get-ten-jokes-by-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Official Joke API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/officialJokeAPI/latest/actions/get-ten-jokes-by-type?connectionId=$CONNECTION_ID&type=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "type": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/officialJokeAPI/latest/actions/get-ten-jokes-by-type?${params}`, {
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
| `type` | string | yes | Joke type returned by List Joke Types. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "punchline": "string",
      "setup": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Provider joke identifier. |
| `punchline` | string | Joke punchline. |
| `setup` | string | Joke setup. |
| `type` | string | Provider joke type. |

## Native endpoint

Through the native Official Joke API API, this operation is `GET /jokes/:type/ten` (base URL `https://official-joke-api.appspot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ten-jokes-by-type.md) for the provider-specific parameters and requirements.

