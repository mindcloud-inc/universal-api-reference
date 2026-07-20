# Ritekit: Get Hashtag Suggestions For URL

Retrieves Ritekit hashtag suggestions for a URL.

```
GET https://connect.mindcloud.co/v1/universal/ritekit/latest/actions/get-hashtag-suggestions-for-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ritekit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ritekit/latest/actions/get-hashtag-suggestions-for-url?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ritekit/latest/actions/get-hashtag-suggestions-for-url?${params}`, {
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
| `url` | string | yes | URL to analyze for hashtag suggestions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hashtags": [
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
| `hashtags` | array<object> |  |
| `message` | string |  |
| `result` | boolean |  |

## Native endpoint

Through the native Ritekit API, this operation is `GET /v2/stats/hashtags-for-url` (base URL `https://api.ritekit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-hashtag-suggestions-for-url.md) for the provider-specific parameters and requirements.

