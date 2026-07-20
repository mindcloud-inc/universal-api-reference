# NewsBlur: Get Original Story

Retrieves a story's original webpage from NewsBlur.

```
GET https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/get-original-story
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NewsBlur `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/get-original-story?connectionId=$CONNECTION_ID&storyHash=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "storyHash": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/get-original-story?${params}`, {
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
| `storyHash` | string | yes | Story hash to fetch the original website story for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "html": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `html` | string | Original story HTML returned by NewsBlur. |

## Native endpoint

Through the native NewsBlur API, this operation is `GET /rss_feeds/original_story` (base URL `https://www.newsblur.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-original-story.md) for the provider-specific parameters and requirements.

