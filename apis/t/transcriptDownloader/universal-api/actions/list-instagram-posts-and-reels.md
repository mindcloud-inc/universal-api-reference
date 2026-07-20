# Transcript Downloader: List Instagram Posts and Reels

Retrieves Instagram posts and reels from Transcript Downloader.

```
GET https://connect.mindcloud.co/v1/universal/transcriptDownloader/latest/actions/list-instagram-posts-and-reels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transcript Downloader `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/transcriptDownloader/latest/actions/list-instagram-posts-and-reels?connectionId=$CONNECTION_ID&listId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/transcriptDownloader/latest/actions/list-instagram-posts-and-reels?${params}`, {
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
| `listId` | string | yes | The list ID returned by the Instagram profile action. |
| `maxAgeDays` | number | no | Only return posts and reels newer than this many days. |
| `includeWebhook` | string | no | A public webhook URL to receive the completed result. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "downloads": {
        "posts": {
          "cost": "string",
          "id": "string",
          "status": "string",
          "type": "string"
        },
        "reels": {
          "cost": "string",
          "id": "string",
          "status": "string",
          "type": "string"
        }
      },
      "message": "string",
      "posts": [
        {
          "account": "string",
          "audio": [
            "string"
          ],
          "caption": "string",
          "comments": 1,
          "contentType": "string",
          "datePosted": "string",
          "datetime": "string",
          "description": "string",
          "images": [
            "string"
          ],
          "imageUrl": "https://example.com",
          "instagramId": "string",
          "likes": 1,
          "location": {
            "name": "Ava Chen"
          },
          "numComments": 1,
          "photos": [
            "string"
          ],
          "photosNumber": 1,
          "postId": "string",
          "shortcode": "string",
          "type": "string",
          "url": "https://example.com",
          "userPosted": "string",
          "videos": [
            "string"
          ],
          "videosDuration": 1,
          "videoUrl": "https://example.com"
        }
      ],
      "postsCount": 1,
      "reels": [
        {
          "account": "string",
          "contentId": "string",
          "contentType": "string",
          "datePosted": "string",
          "description": "string",
          "isVerified": true,
          "length": 1,
          "likes": 1,
          "numComments": 1,
          "postId": "string",
          "productType": "string",
          "shortcode": "string",
          "thumbnail": "string",
          "type": "string",
          "url": "https://example.com",
          "userPosted": "string",
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
      "reelsCount": 1,
      "status": "string",
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `downloads` | object |  |
| `downloads.posts` | object |  |
| `downloads.posts.cost` | string |  |
| `downloads.posts.id` | string |  |
| `downloads.posts.status` | string |  |
| `downloads.posts.type` | string |  |
| `downloads.reels` | object |  |
| `downloads.reels.cost` | string |  |
| `downloads.reels.id` | string |  |
| `downloads.reels.status` | string |  |
| `downloads.reels.type` | string |  |
| `message` | string |  |
| `posts` | array<object> |  |
| `posts[].account` | string |  |
| `posts[].audio` | array<string> |  |
| `posts[].caption` | string |  |
| `posts[].comments` | number |  |
| `posts[].contentType` | string |  |
| `posts[].datePosted` | string |  |
| `posts[].datetime` | string |  |
| `posts[].description` | string |  |
| `posts[].images` | array<string> |  |
| `posts[].imageUrl` | string |  |
| `posts[].instagramId` | string |  |
| `posts[].likes` | number |  |
| `posts[].location` | object |  |
| `posts[].location.name` | string |  |
| `posts[].numComments` | number |  |
| `posts[].photos` | array<string> |  |
| `posts[].photosNumber` | number |  |
| `posts[].postId` | string |  |
| `posts[].shortcode` | string |  |
| `posts[].type` | string |  |
| `posts[].url` | string |  |
| `posts[].userPosted` | string |  |
| `posts[].videos` | array<string> |  |
| `posts[].videosDuration` | number |  |
| `posts[].videoUrl` | string |  |
| `postsCount` | number |  |
| `reels` | array<object> |  |
| `reels[].account` | string |  |
| `reels[].contentId` | string |  |
| `reels[].contentType` | string |  |
| `reels[].datePosted` | string |  |
| `reels[].description` | string |  |
| `reels[].isVerified` | boolean |  |
| `reels[].length` | number |  |
| `reels[].likes` | number |  |
| `reels[].numComments` | number |  |
| `reels[].postId` | string |  |
| `reels[].productType` | string |  |
| `reels[].shortcode` | string |  |
| `reels[].thumbnail` | string |  |
| `reels[].type` | string |  |
| `reels[].url` | string |  |
| `reels[].userPosted` | string |  |
| `reels[].videoPlayCount` | number |  |
| `reels[].videos` | array<string> |  |
| `reels[].videosDuration` | number |  |
| `reels[].videoUrl` | string |  |
| `reels[].videoViewCount` | number |  |
| `reels[].views` | number |  |
| `reelsCount` | number |  |
| `status` | string |  |
| `totalCount` | number |  |

## Native endpoint

Through the native Transcript Downloader API, this operation is `POST /api/instagram/list` (base URL `https://dashboard.transcriptdownloader.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-instagram-posts-and-reels.md) for the provider-specific parameters and requirements.

