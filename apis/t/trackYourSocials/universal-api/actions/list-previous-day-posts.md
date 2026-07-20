# TrackYourSocials: List Previous Day Posts

Retrieves yesterday's posts from a social media channel in TrackYourSocials.

```
GET https://connect.mindcloud.co/v1/universal/trackYourSocials/latest/actions/list-previous-day-posts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrackYourSocials `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trackYourSocials/latest/actions/list-previous-day-posts?connectionId=$CONNECTION_ID&userAccount=https%3A%2F%2Fwww.instagram.com%2Fnasa%2F" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userAccount": "https://www.instagram.com/nasa/"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trackYourSocials/latest/actions/list-previous-day-posts?${params}`, {
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
| `userAccount` | string | yes | URL of the social media channel to fetch yesterday's posts from. Example: `https://www.instagram.com/nasa/`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "posts": {
        "caption": "string",
        "link": "https://example.com",
        "name": "Ava Chen"
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
| `success` | boolean |  |

## Native endpoint

Through the native TrackYourSocials API, this operation is `GET /api/v1/previous-day-posts` (base URL `https://trackyoursocials.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-previous-day-posts.md) for the provider-specific parameters and requirements.

