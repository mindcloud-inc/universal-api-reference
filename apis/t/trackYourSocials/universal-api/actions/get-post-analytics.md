# TrackYourSocials: Get Post Analytics

Retrieves engagement metrics for a social media post from TrackYourSocials.

```
GET https://connect.mindcloud.co/v1/universal/trackYourSocials/latest/actions/get-post-analytics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrackYourSocials `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trackYourSocials/latest/actions/get-post-analytics?connectionId=$CONNECTION_ID&mediaLink=https%3A%2F%2Finstagram.com%2Fp%2FABC123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mediaLink": "https://instagram.com/p/ABC123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trackYourSocials/latest/actions/get-post-analytics?${params}`, {
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
| `mediaLink` | string | yes | URL of the social media content to analyze. Example: `https://instagram.com/p/ABC123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comments": 1,
      "Likes": 1,
      "platform": "string",
      "post": "string",
      "success": true,
      "thumbnail": "string",
      "views": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comments` | number |  |
| `Likes` | number |  |
| `platform` | string |  |
| `post` | string |  |
| `success` | boolean |  |
| `thumbnail` | string |  |
| `views` | number |  |

## Native endpoint

Through the native TrackYourSocials API, this operation is `GET /api/v1/analytics` (base URL `https://trackyoursocials.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-post-analytics.md) for the provider-specific parameters and requirements.

