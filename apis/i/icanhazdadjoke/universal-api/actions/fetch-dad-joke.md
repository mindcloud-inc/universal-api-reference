# icanhazdadjoke: Fetch Dad Joke

Retrieves a specific dad joke from icanhazdadjoke.

```
GET https://connect.mindcloud.co/v1/universal/icanhazdadjoke/latest/actions/fetch-dad-joke
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a icanhazdadjoke `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/icanhazdadjoke/latest/actions/fetch-dad-joke?connectionId=$CONNECTION_ID&jokeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jokeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/icanhazdadjoke/latest/actions/fetch-dad-joke?${params}`, {
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
| `jokeId` | string | yes | ID of the dad joke to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "joke": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Dad joke ID. |
| `joke` | string | Dad joke text. |
| `status` | number | HTTP-style status from the API response. |

## Native endpoint

Through the native icanhazdadjoke API, this operation is `GET /j/:jokeId` (base URL `https://icanhazdadjoke.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-dad-joke.md) for the provider-specific parameters and requirements.

