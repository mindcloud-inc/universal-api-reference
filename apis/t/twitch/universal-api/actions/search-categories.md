# Twitch: Search Categories

Searches Twitch categories using a query.

```
GET https://connect.mindcloud.co/v1/universal/twitch/latest/actions/search-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twitch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twitch/latest/actions/search-categories?connectionId=$CONNECTION_ID&searchQuery=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "searchQuery": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twitch/latest/actions/search-categories?${params}`, {
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
| `searchQuery` | string | yes | The URI-encoded search string. |
| `first` | number | no | The maximum number of objects to return. Maximum: 100. Default: 20. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `after` | string | no | The cursor used to get the next page of results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "boxArtUrl": "https://example.com",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `boxArtUrl` | string |  |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Twitch API, this operation is `GET /search/categories` (base URL `https://api.twitch.tv/helix`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-categories.md) for the provider-specific parameters and requirements.

