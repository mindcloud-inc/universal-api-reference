# Scrape Creators: Get Linktree Page

Retrieves a Linktree page from Scrape Creators.

```
GET https://connect.mindcloud.co/v1/universal/scrapeCreators/latest/actions/get-linktree-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrape Creators `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeCreators/latest/actions/get-linktree-page?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeCreators/latest/actions/get-linktree-page?${params}`, {
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
| `url` | string | yes | Linktree URL |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apple_music": "string",
      "credits_remaining": 1,
      "description": "string",
      "email_address": "ava@example.com",
      "id": 1,
      "instagram": "string",
      "linkPlatforms": [
        "https://example.com"
      ],
      "links": [
        {}
      ],
      "profilePictureUrl": "https://example.com",
      "soundcloud": "string",
      "spotify": "string",
      "success": true,
      "tiktok": "string",
      "timezone": "string",
      "username": "Ava Chen",
      "verticals": [
        "string"
      ],
      "youtube": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apple_music` | string |  |
| `credits_remaining` | number |  |
| `description` | string |  |
| `email_address` | string |  |
| `id` | number |  |
| `instagram` | string |  |
| `linkPlatforms` | array<string> |  |
| `links` | array<object> |  |
| `profilePictureUrl` | string |  |
| `soundcloud` | string |  |
| `spotify` | string |  |
| `success` | boolean |  |
| `tiktok` | string |  |
| `timezone` | string |  |
| `username` | string |  |
| `verticals` | array<string> |  |
| `youtube` | string |  |

## Native endpoint

Through the native Scrape Creators API, this operation is `GET /v1/linktree` (base URL `https://api.scrapecreators.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-linktree-page.md) for the provider-specific parameters and requirements.

