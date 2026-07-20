# ScrapingBot: Get Instagram User by ID



```
GET https://connect.mindcloud.co/v1/universal/scrapingBot/latest/actions/get-instagram-user-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingBot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingBot/latest/actions/get-instagram-user-by-id?connectionId=$CONNECTION_ID&id=25025320" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "25025320"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingBot/latest/actions/get-instagram-user-by-id?${params}`, {
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
| `id` | string | yes | Instagram user ID. Default: `25025320`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "biography": "string",
      "creditsUsed": 1,
      "duration": "string",
      "follower_count": 1,
      "following_count": 1,
      "full_name": "Ava Chen",
      "id": "string",
      "is_verified": true,
      "media_count": 1,
      "profile_pic_url": "https://example.com",
      "statusCode": 1,
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
| `creditsUsed` | number |  |
| `duration` | string |  |
| `follower_count` | number |  |
| `following_count` | number |  |
| `full_name` | string |  |
| `id` | string |  |
| `is_verified` | boolean |  |
| `media_count` | number |  |
| `profile_pic_url` | string |  |
| `statusCode` | number |  |
| `username` | string |  |

## Native endpoint

Through the native ScrapingBot API, this operation is `POST /instagram` (base URL `https://scrapingbot.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-instagram-user-by-id.md) for the provider-specific parameters and requirements.

