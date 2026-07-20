# Scrape Creators: Get Instagram Basic Profile

Retrieves an Instagram basic profile from Scrape Creators.

```
GET https://connect.mindcloud.co/v1/universal/scrapeCreators/latest/actions/get-instagram-basic-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrape Creators `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeCreators/latest/actions/get-instagram-basic-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeCreators/latest/actions/get-instagram-basic-profile?${params}`, {
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
| `userId` | string | no | Instagram user id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "biography": "string",
      "credits_remaining": 1,
      "follower_count": 1,
      "following_count": 1,
      "full_name": "Ava Chen",
      "id": "string",
      "media_count": 1,
      "profile_pic_url": "https://example.com",
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
| `biography` | string |  |
| `credits_remaining` | number |  |
| `follower_count` | number |  |
| `following_count` | number |  |
| `full_name` | string |  |
| `id` | string |  |
| `media_count` | number |  |
| `profile_pic_url` | string |  |
| `success` | boolean |  |
| `username` | string |  |

## Native endpoint

Through the native Scrape Creators API, this operation is `GET /v1/instagram/basic-profile` (base URL `https://api.scrapecreators.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-instagram-basic-profile.md) for the provider-specific parameters and requirements.

