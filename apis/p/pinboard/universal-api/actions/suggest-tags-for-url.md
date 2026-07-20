# Pinboard: Suggest Tags For URL



```
GET https://connect.mindcloud.co/v1/universal/pinboard/latest/actions/suggest-tags-for-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinboard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinboard/latest/actions/suggest-tags-for-url?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinboard/latest/actions/suggest-tags-for-url?${params}`, {
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
| `url` | string | yes | URL to suggest tags for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "popular": [
        "string"
      ],
      "recommended": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `popular` | array<string> | Popular tags used site-wide for the URL. |
| `recommended` | array<string> | Recommended tags from the user's own tagging history. |

## Native endpoint

Through the native Pinboard API, this operation is `GET /posts/suggest` (base URL `https://api.pinboard.in/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/suggest-tags-for-url.md) for the provider-specific parameters and requirements.

