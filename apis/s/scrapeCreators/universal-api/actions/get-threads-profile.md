# Scrape Creators: Get Threads Profile

Retrieves a Threads profile from Scrape Creators.

```
GET https://connect.mindcloud.co/v1/universal/scrapeCreators/latest/actions/get-threads-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrape Creators `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeCreators/latest/actions/get-threads-profile?connectionId=$CONNECTION_ID&handle=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "handle": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeCreators/latest/actions/get-threads-profile?${params}`, {
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
| `handle` | string | yes | Threads handle |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bio_links": [
        {}
      ],
      "biography": "string",
      "credits_remaining": 1,
      "follower_count": 1,
      "full_name": "Ava Chen",
      "id": "string",
      "is_verified": true,
      "profile_pic_url": "https://example.com",
      "show_text_post_app_badge": true,
      "success": true,
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bio_links` | array<object> |  |
| `biography` | string |  |
| `credits_remaining` | number |  |
| `follower_count` | number |  |
| `full_name` | string |  |
| `id` | string |  |
| `is_verified` | boolean |  |
| `profile_pic_url` | string |  |
| `show_text_post_app_badge` | boolean |  |
| `success` | boolean |  |
| `username` | string |  |

## Native endpoint

Through the native Scrape Creators API, this operation is `GET /v1/threads/profile` (base URL `https://api.scrapecreators.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-threads-profile.md) for the provider-specific parameters and requirements.

