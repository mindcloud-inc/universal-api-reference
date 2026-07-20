# Tumblr: Get Blog Info

Retrieves information for a Tumblr blog.

```
GET https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/get-blog-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tumblr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/get-blog-info?connectionId=$CONNECTION_ID&blogIdentifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "blogIdentifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/get-blog-info?${params}`, {
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
| `blogIdentifier` | string | yes | Any blog identifier. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields.blogs` | string | no | Comma-separated blog fields for a partial response. Example: `name,updated`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blog": {
        "admin": true,
        "ask": true,
        "askAnon": true,
        "askPageTitle": "string",
        "asksAllowMedia": true,
        "avatar": [
          {
            "height": 1,
            "url": "https://example.com",
            "width": 1
          }
        ],
        "canChat": true,
        "canSendFanMail": true,
        "canSubscribe": true,
        "description": "string",
        "drafts": 1,
        "facebook": "string",
        "facebookOpengraphEnabled": "string",
        "followed": true,
        "followers": 1,
        "isBlockedFromPrimary": true,
        "isNsfw": true,
        "likes": 1,
        "messages": 1,
        "name": "Ava Chen",
        "posts": 1,
        "primary": true,
        "queue": 1,
        "shareLikes": true,
        "subscribed": true,
        "theme": {
          "avatarShape": "string",
          "backgroundColor": "string",
          "bodyFont": "string",
          "headerBounds": "string",
          "headerImage": "string",
          "headerImageFocused": "string",
          "headerImagePoster": "string",
          "headerImageScaled": "string",
          "headerStretch": true,
          "linkColor": "https://example.com",
          "showAvatar": true,
          "showDescription": true,
          "showHeaderImage": true,
          "showTitle": true,
          "titleColor": "string",
          "titleFont": "string",
          "titleFontWeight": "string"
        },
        "themeId": 1,
        "title": "string",
        "totalPosts": 1,
        "tweet": "string",
        "twitterEnabled": true,
        "twitterSend": true,
        "type": "string",
        "updated": 1,
        "url": "https://example.com",
        "uuid": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blog.admin` | boolean |  |
| `blog.ask` | boolean |  |
| `blog.askAnon` | boolean |  |
| `blog.askPageTitle` | string |  |
| `blog.asksAllowMedia` | boolean |  |
| `blog.avatar[].height` | number |  |
| `blog.avatar[].url` | string |  |
| `blog.avatar[].width` | number |  |
| `blog.canChat` | boolean |  |
| `blog.canSendFanMail` | boolean |  |
| `blog.canSubscribe` | boolean |  |
| `blog.description` | string |  |
| `blog.drafts` | number |  |
| `blog.facebook` | string |  |
| `blog.facebookOpengraphEnabled` | string |  |
| `blog.followed` | boolean |  |
| `blog.followers` | number |  |
| `blog.isBlockedFromPrimary` | boolean |  |
| `blog.isNsfw` | boolean |  |
| `blog.likes` | number |  |
| `blog.messages` | number |  |
| `blog.name` | string |  |
| `blog.posts` | number |  |
| `blog.primary` | boolean |  |
| `blog.queue` | number |  |
| `blog.shareLikes` | boolean |  |
| `blog.subscribed` | boolean |  |
| `blog.theme.avatarShape` | string |  |
| `blog.theme.backgroundColor` | string |  |
| `blog.theme.bodyFont` | string |  |
| `blog.theme.headerBounds` | string |  |
| `blog.theme.headerImage` | string |  |
| `blog.theme.headerImageFocused` | string |  |
| `blog.theme.headerImagePoster` | string |  |
| `blog.theme.headerImageScaled` | string |  |
| `blog.theme.headerStretch` | boolean |  |
| `blog.theme.linkColor` | string |  |
| `blog.theme.showAvatar` | boolean |  |
| `blog.theme.showDescription` | boolean |  |
| `blog.theme.showHeaderImage` | boolean |  |
| `blog.theme.showTitle` | boolean |  |
| `blog.theme.titleColor` | string |  |
| `blog.theme.titleFont` | string |  |
| `blog.theme.titleFontWeight` | string |  |
| `blog.themeId` | number |  |
| `blog.title` | string |  |
| `blog.totalPosts` | number |  |
| `blog.tweet` | string |  |
| `blog.twitterEnabled` | boolean |  |
| `blog.twitterSend` | boolean |  |
| `blog.type` | string |  |
| `blog.updated` | number |  |
| `blog.url` | string |  |
| `blog.uuid` | string |  |

## Native endpoint

Through the native Tumblr API, this operation is `GET /v2/blog/:blogIdentifier/info` (base URL `https://api.tumblr.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-blog-info.md) for the provider-specific parameters and requirements.

