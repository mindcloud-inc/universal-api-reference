# Giphy: Autocomplete GIF Tags

Finds autocomplete tag terms for GIFs in Giphy.

```
GET https://connect.mindcloud.co/v1/universal/giphy/latest/actions/autocomplete-gif-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Giphy `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/giphy/latest/actions/autocomplete-gif-tags?connectionId=$CONNECTION_ID&limit=25&offset=0&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/giphy/latest/actions/autocomplete-gif-tags?${params}`, {
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
| `q` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "analyticsResponsePayload": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `analyticsResponsePayload` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Giphy API, this operation is `GET /v1/gifs/search/tags` (base URL `https://api.giphy.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/autocomplete-gif-tags.md) for the provider-specific parameters and requirements.

