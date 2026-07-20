# Scrape Creators: Get Facebook Profile

Retrieves a Facebook profile from Scrape Creators.

```
GET https://connect.mindcloud.co/v1/universal/scrapeCreators/latest/actions/get-facebook-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrape Creators `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeCreators/latest/actions/get-facebook-profile?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeCreators/latest/actions/get-facebook-profile?${params}`, {
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
| `url` | string | yes | Facebook profile URL |
| `getBusinessHours` | boolean | no | Include business hours when available |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "adLibrary": {},
      "businessHours": [
        {}
      ],
      "category": "string",
      "coverPhoto": {},
      "creationDate": "string",
      "credits_remaining": 1,
      "email": "ava@example.com",
      "followerCount": 1,
      "id": "string",
      "isBusinessPageActive": true,
      "likeCount": 1,
      "name": "Ava Chen",
      "pageIntro": "string",
      "phone": "string",
      "priceRange": "string",
      "profilePhoto": {},
      "profilePicLarge": "string",
      "profilePicMedium": "string",
      "profilePicSmall": "string",
      "rating": "string",
      "services": "string",
      "success": true,
      "url": "https://example.com",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `adLibrary` | object |  |
| `businessHours` | array<object> |  |
| `category` | string |  |
| `coverPhoto` | object |  |
| `creationDate` | string |  |
| `credits_remaining` | number |  |
| `email` | string |  |
| `followerCount` | number |  |
| `id` | string |  |
| `isBusinessPageActive` | boolean |  |
| `likeCount` | number |  |
| `name` | string |  |
| `pageIntro` | string |  |
| `phone` | string |  |
| `priceRange` | string |  |
| `profilePhoto` | object |  |
| `profilePicLarge` | string |  |
| `profilePicMedium` | string |  |
| `profilePicSmall` | string |  |
| `rating` | string |  |
| `services` | string |  |
| `success` | boolean |  |
| `url` | string |  |
| `website` | string |  |

## Native endpoint

Through the native Scrape Creators API, this operation is `GET /v1/facebook/profile` (base URL `https://api.scrapecreators.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-facebook-profile.md) for the provider-specific parameters and requirements.

