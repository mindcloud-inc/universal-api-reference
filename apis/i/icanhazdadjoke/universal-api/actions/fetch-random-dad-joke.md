# icanhazdadjoke: Fetch Random Dad Joke

Retrieves a random dad joke from icanhazdadjoke.

```
GET https://connect.mindcloud.co/v1/universal/icanhazdadjoke/latest/actions/fetch-random-dad-joke
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a icanhazdadjoke `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/icanhazdadjoke/latest/actions/fetch-random-dad-joke?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/icanhazdadjoke/latest/actions/fetch-random-dad-joke?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native icanhazdadjoke API, this operation is `GET /` (base URL `https://icanhazdadjoke.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-random-dad-joke.md) for the provider-specific parameters and requirements.

