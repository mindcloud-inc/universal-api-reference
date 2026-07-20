# Raindrop: Parse URL



```
GET https://connect.mindcloud.co/v1/universal/raindrop/latest/actions/parse-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raindrop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/raindrop/latest/actions/parse-url?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/raindrop/latest/actions/parse-url?${params}`, {
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
| `url` | string | no | URL to parse for metadata. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": "string",
      "errorMessage": "string",
      "item": {
        "cover": "string",
        "excerpt": "string",
        "media": [
          {
            "link": "https://example.com",
            "type": "string"
          }
        ],
        "meta": {
          "canonical": "string",
          "possibleArticle": true,
          "site": "string",
          "tags": [
            "string"
          ]
        },
        "parser": "string",
        "title": "string",
        "type": "string"
      },
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | string |  |
| `errorMessage` | string |  |
| `item` | object |  |
| `item.cover` | string |  |
| `item.excerpt` | string |  |
| `item.media` | array<object> |  |
| `item.media[].link` | string |  |
| `item.media[].type` | string |  |
| `item.meta` | object |  |
| `item.meta.canonical` | string |  |
| `item.meta.possibleArticle` | boolean |  |
| `item.meta.site` | string |  |
| `item.meta.tags` | array<string> |  |
| `item.parser` | string |  |
| `item.title` | string |  |
| `item.type` | string |  |
| `result` | boolean |  |

## Native endpoint

Through the native Raindrop API, this operation is `GET /import/url/parse` (base URL `https://api.raindrop.io/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/parse-url.md) for the provider-specific parameters and requirements.

