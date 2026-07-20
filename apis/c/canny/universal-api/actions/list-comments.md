# Canny: List Comments

Retrieves all available comments from Canny.

```
GET https://connect.mindcloud.co/v1/universal/canny/latest/actions/list-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Canny `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/canny/latest/actions/list-comments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/canny/latest/actions/list-comments?${params}`, {
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
      "author": {},
      "board": {},
      "created": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "imageURLs": [
        "https://example.com"
      ],
      "internal": true,
      "likeCount": 1,
      "mentions": [
        {}
      ],
      "parentID": "string",
      "post": {},
      "private": true,
      "reactions": {},
      "status": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | object |  |
| `board` | object |  |
| `created` | date |  |
| `id` | string |  |
| `imageURLs` | array<string> |  |
| `internal` | boolean |  |
| `likeCount` | number |  |
| `mentions` | array<object> |  |
| `parentID` | string |  |
| `post` | object |  |
| `private` | boolean |  |
| `reactions` | object |  |
| `status` | string |  |
| `value` | string |  |

## Native endpoint

Through the native Canny API, this operation is `POST /v1/comments/list` (base URL `https://canny.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-comments.md) for the provider-specific parameters and requirements.

