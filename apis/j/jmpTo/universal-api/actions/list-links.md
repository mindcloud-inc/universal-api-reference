# JmpTo: List Links

Retrieves links from JmpTo.

```
GET https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/list-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JmpTo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/list-links?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/list-links?${params}`, {
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
| `order` | string | no | Sort order for returned links. JmpTo's example uses date. |
| `q` | string | no | Search links using a keyword. |
| `short` | string | no | Search using the short URL. When this is used, other parameters are ignored and a single-link response may be returned. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alias": "string",
      "clicks": 1,
      "date": "string",
      "description": "string",
      "id": 1,
      "longurl": "https://example.com",
      "shorturl": "https://example.com",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alias` | string |  |
| `clicks` | number |  |
| `date` | string |  |
| `description` | string |  |
| `id` | number |  |
| `longurl` | string |  |
| `shorturl` | string |  |
| `title` | string |  |

## Native endpoint

Through the native JmpTo API, this operation is `GET /urls` (base URL `https://jmpto.net/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-links.md) for the provider-specific parameters and requirements.

