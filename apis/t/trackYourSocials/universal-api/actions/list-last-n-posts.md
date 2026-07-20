# TrackYourSocials: List Last N Posts

Retrieves the last N posts from a social profile in TrackYourSocials.

```
GET https://connect.mindcloud.co/v1/universal/trackYourSocials/latest/actions/list-last-n-posts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrackYourSocials `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trackYourSocials/latest/actions/list-last-n-posts?connectionId=$CONNECTION_ID&userAccount=%40handle%20(or%20full%20URL)" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userAccount": "@handle (or full URL)"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trackYourSocials/latest/actions/list-last-n-posts?${params}`, {
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
| `n` | number | no | Number of posts to return. Supported range: 1 to 200. Default: `10`. Example: `10`. |
| `userAccount` | string | yes | Profile URL or handle for the social media account. Example: `@handle (or full URL)`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "posts": {
        "caption": "string",
        "link": "https://example.com",
        "name": "Ava Chen",
        "platform": "string",
        "posted_at": "2026-05-07T12:00:00.000Z"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `posts.caption` | string |  |
| `posts.link` | string |  |
| `posts.name` | string |  |
| `posts.platform` | string |  |
| `posts.posted_at` | date |  |
| `success` | boolean |  |

## Native endpoint

Through the native TrackYourSocials API, this operation is `GET /api/v1/last-n-posts` (base URL `https://trackyoursocials.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-last-n-posts.md) for the provider-specific parameters and requirements.

