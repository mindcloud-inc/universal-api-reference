# Ritekit: Get Hashtag Suggestions For Image

Retrieves Ritekit hashtag suggestions for an image.

```
GET https://connect.mindcloud.co/v1/universal/ritekit/latest/actions/get-hashtag-suggestions-for-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ritekit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ritekit/latest/actions/get-hashtag-suggestions-for-image?connectionId=$CONNECTION_ID&imageUrl=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "imageUrl": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ritekit/latest/actions/get-hashtag-suggestions-for-image?${params}`, {
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
| `imageUrl` | string | yes | Public image URL to analyze for hashtag suggestions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": [
        {}
      ],
      "message": "string",
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `data` | array<object> |  |
| `message` | string |  |
| `result` | boolean |  |

## Native endpoint

Through the native Ritekit API, this operation is `GET /v1/stats/hashtag-suggestions-image` (base URL `https://api.ritekit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-hashtag-suggestions-for-image.md) for the provider-specific parameters and requirements.

