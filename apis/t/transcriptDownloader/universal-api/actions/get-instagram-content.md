# Transcript Downloader: Get Instagram Content

Retrieves Instagram content metadata from Transcript Downloader.

```
GET https://connect.mindcloud.co/v1/universal/transcriptDownloader/latest/actions/get-instagram-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transcript Downloader `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/transcriptDownloader/latest/actions/get-instagram-content?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/transcriptDownloader/latest/actions/get-instagram-content?${params}`, {
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
| `url` | string | yes | The Instagram post or reel URL. |
| `includeWebhook` | string | no | A public webhook URL to receive the completed result. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": "string",
      "altText": "string",
      "audio": [
        "string"
      ],
      "caption": "string",
      "coauthorProducers": [
        "string"
      ],
      "comments": 1,
      "contentId": "string",
      "contentType": "string",
      "datePosted": "string",
      "datetime": "string",
      "description": "string",
      "followers": 1,
      "hashtags": [
        "string"
      ],
      "images": [
        "string"
      ],
      "imageUrl": "https://example.com",
      "instagramId": "string",
      "isPaidPartnership": true,
      "isPinned": true,
      "isVerified": true,
      "latestComments": [
        {
          "comment": "string",
          "createdAt": "string",
          "dateOfComment": "string",
          "likes": 1,
          "userCommenting": "string"
        }
      ],
      "length": 1,
      "likes": 1,
      "location": {
        "name": "Ava Chen"
      },
      "numComments": 1,
      "partnershipDetails": [
        "string"
      ],
      "photos": [
        "string"
      ],
      "photosNumber": 1,
      "pk": "string",
      "postContent": [
        {
          "index": 1,
          "instagramId": "string",
          "type": "string",
          "url": "https://example.com"
        }
      ],
      "postId": "string",
      "postsCount": 1,
      "productType": "string",
      "profileImageLink": "https://example.com",
      "profileUrl": "https://example.com",
      "shortcode": "string",
      "source": "string",
      "status": "string",
      "taggedUsers": [
        {
          "fullName": "Ava Chen",
          "isVerified": true,
          "username": "Ava Chen"
        }
      ],
      "thumbnail": "string",
      "timestamp": "string",
      "type": "string",
      "url": "https://example.com",
      "userPosted": "string",
      "userPostedId": "string",
      "videoPlayCount": 1,
      "videos": [
        "string"
      ],
      "videosDuration": 1,
      "videoUrl": "https://example.com",
      "videoViewCount": 1,
      "views": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | string |  |
| `altText` | string |  |
| `audio` | array<string> |  |
| `caption` | string |  |
| `coauthorProducers` | array<string> |  |
| `comments` | number |  |
| `contentId` | string |  |
| `contentType` | string |  |
| `datePosted` | string |  |
| `datetime` | string |  |
| `description` | string |  |
| `followers` | number |  |
| `hashtags` | array<string> |  |
| `images` | array<string> |  |
| `imageUrl` | string |  |
| `instagramId` | string |  |
| `isPaidPartnership` | boolean |  |
| `isPinned` | boolean |  |
| `isVerified` | boolean |  |
| `latestComments` | array<object> |  |
| `latestComments[].comment` | string |  |
| `latestComments[].createdAt` | string |  |
| `latestComments[].dateOfComment` | string |  |
| `latestComments[].likes` | number |  |
| `latestComments[].userCommenting` | string |  |
| `length` | number |  |
| `likes` | number |  |
| `location` | object |  |
| `location.name` | string |  |
| `numComments` | number |  |
| `partnershipDetails` | array<string> |  |
| `photos` | array<string> |  |
| `photosNumber` | number |  |
| `pk` | string |  |
| `postContent` | array<object> |  |
| `postContent[].index` | number |  |
| `postContent[].instagramId` | string |  |
| `postContent[].type` | string |  |
| `postContent[].url` | string |  |
| `postId` | string |  |
| `postsCount` | number |  |
| `productType` | string |  |
| `profileImageLink` | string |  |
| `profileUrl` | string |  |
| `shortcode` | string |  |
| `source` | string |  |
| `status` | string |  |
| `taggedUsers` | array<object> |  |
| `taggedUsers[].fullName` | string |  |
| `taggedUsers[].isVerified` | boolean |  |
| `taggedUsers[].username` | string |  |
| `thumbnail` | string |  |
| `timestamp` | string |  |
| `type` | string |  |
| `url` | string |  |
| `userPosted` | string |  |
| `userPostedId` | string |  |
| `videoPlayCount` | number |  |
| `videos` | array<string> |  |
| `videosDuration` | number |  |
| `videoUrl` | string |  |
| `videoViewCount` | number |  |
| `views` | number |  |

## Native endpoint

Through the native Transcript Downloader API, this operation is `POST /api/instagram/content` (base URL `https://dashboard.transcriptdownloader.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-instagram-content.md) for the provider-specific parameters and requirements.

