# Raindrop: Search Collection Covers



```
GET https://connect.mindcloud.co/v1/universal/raindrop/latest/actions/search-collection-covers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raindrop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/raindrop/latest/actions/search-collection-covers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/raindrop/latest/actions/search-collection-covers?${params}`, {
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
| `text` | string | no | The text prompt used to search collection covers. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {
          "icons": [
            {
              "png": "string",
              "svg": "string"
            }
          ],
          "title": "string"
        }
      ],
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> |  |
| `items[].icons` | array<object> |  |
| `items[].icons[].png` | string |  |
| `items[].icons[].svg` | string |  |
| `items[].title` | string |  |
| `result` | boolean |  |

## Native endpoint

Through the native Raindrop API, this operation is `GET /collections/covers/:text` (base URL `https://api.raindrop.io/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-collection-covers.md) for the provider-specific parameters and requirements.

