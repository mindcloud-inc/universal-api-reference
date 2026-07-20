# Tumblr: Unfollow Blog

Unfollows a Tumblr blog from the user account.

```
DELETE https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/unfollow-blog
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tumblr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/unfollow-blog?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/unfollow-blog?${params}`, {
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
| `url` | string | yes | The URL of the blog to unfollow. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blog": {
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
        "followed": true,
        "isBlockedFromPrimary": true,
        "isNsfw": true,
        "name": "Ava Chen",
        "posts": 1,
        "shareLikes": true,
        "subscribed": true,
        "theme": {
          "avatarShape": "string",
          "backgroundColor": "string",
          "bodyFont": "string",
          "headerBounds": "string",
          "headerFullHeight": 1,
          "headerFullWidth": 1,
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
| `blog.followed` | boolean |  |
| `blog.isBlockedFromPrimary` | boolean |  |
| `blog.isNsfw` | boolean |  |
| `blog.name` | string |  |
| `blog.posts` | number |  |
| `blog.shareLikes` | boolean |  |
| `blog.subscribed` | boolean |  |
| `blog.theme.avatarShape` | string |  |
| `blog.theme.backgroundColor` | string |  |
| `blog.theme.bodyFont` | string |  |
| `blog.theme.headerBounds` | string |  |
| `blog.theme.headerFullHeight` | number |  |
| `blog.theme.headerFullWidth` | number |  |
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
| `blog.updated` | number |  |
| `blog.url` | string |  |
| `blog.uuid` | string |  |

## Native endpoint

Through the native Tumblr API, this operation is `POST /v2/user/unfollow` (base URL `https://api.tumblr.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unfollow-blog.md) for the provider-specific parameters and requirements.

