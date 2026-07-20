# icanhazdadjoke: Search Dad Jokes

Finds dad jokes in icanhazdadjoke by search term.

```
GET https://connect.mindcloud.co/v1/universal/icanhazdadjoke/latest/actions/search-dad-jokes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a icanhazdadjoke `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/icanhazdadjoke/latest/actions/search-dad-jokes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/icanhazdadjoke/latest/actions/search-dad-jokes?${params}`, {
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
| `term` | string | no | Optional search term to use when searching dad jokes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "joke": "string"
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

## Native endpoint

Through the native icanhazdadjoke API, this operation is `GET /search` (base URL `https://icanhazdadjoke.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-dad-jokes.md) for the provider-specific parameters and requirements.

