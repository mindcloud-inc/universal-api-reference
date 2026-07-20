# NewsBlur: List Favicons

Retrieves feed favicons from NewsBlur.

```
GET https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/list-favicons
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NewsBlur `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/list-favicons?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/list-favicons?${params}`, {
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
| `feedId` | number<number> | no | Feed ID to retrieve a favicon for. NewsBlur supports repeating feed_ids for multiple feeds. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authenticated": true,
      "code": 1,
      "favicons": {},
      "result": "string",
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authenticated` | boolean | Whether the session is authenticated. |
| `code` | number | NewsBlur result code. |
| `favicons` | object | Favicons keyed by feed ID. |
| `result` | string | Result status. |
| `user_id` | number | Authenticated NewsBlur user ID. |

## Native endpoint

Through the native NewsBlur API, this operation is `GET /reader/favicons` (base URL `https://www.newsblur.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-favicons.md) for the provider-specific parameters and requirements.

