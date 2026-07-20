# Tumblr: Get User Information

Retrieves account information for the Tumblr user.

```
GET https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/get-user-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tumblr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/get-user-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/get-user-information?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "user": {
        "blogs": [
          {
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
        ],
        "defaultPostFormat": "string",
        "following": 1,
        "likes": 1,
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `user.blogs[].admin` | boolean |  |
| `user.blogs[].ask` | boolean |  |
| `user.blogs[].askAnon` | boolean |  |
| `user.blogs[].askPageTitle` | string |  |
| `user.blogs[].asksAllowMedia` | boolean |  |
| `user.blogs[].avatar[].height` | number |  |
| `user.blogs[].avatar[].url` | string |  |
| `user.blogs[].avatar[].width` | number |  |
| `user.blogs[].canChat` | boolean |  |
| `user.blogs[].canSendFanMail` | boolean |  |
| `user.blogs[].canSubscribe` | boolean |  |
| `user.blogs[].description` | string |  |
| `user.blogs[].drafts` | number |  |
| `user.blogs[].facebook` | string |  |
| `user.blogs[].facebookOpengraphEnabled` | string |  |
| `user.blogs[].followed` | boolean |  |
| `user.blogs[].followers` | number |  |
| `user.blogs[].isBlockedFromPrimary` | boolean |  |
| `user.blogs[].isNsfw` | boolean |  |
| `user.blogs[].likes` | number |  |
| `user.blogs[].messages` | number |  |
| `user.blogs[].name` | string |  |
| `user.blogs[].posts` | number |  |
| `user.blogs[].primary` | boolean |  |
| `user.blogs[].queue` | number |  |
| `user.blogs[].shareLikes` | boolean |  |
| `user.blogs[].subscribed` | boolean |  |
| `user.blogs[].theme.avatarShape` | string |  |
| `user.blogs[].theme.backgroundColor` | string |  |
| `user.blogs[].theme.bodyFont` | string |  |
| `user.blogs[].theme.headerBounds` | string |  |
| `user.blogs[].theme.headerImage` | string |  |
| `user.blogs[].theme.headerImageFocused` | string |  |
| `user.blogs[].theme.headerImagePoster` | string |  |
| `user.blogs[].theme.headerImageScaled` | string |  |
| `user.blogs[].theme.headerStretch` | boolean |  |
| `user.blogs[].theme.linkColor` | string |  |
| `user.blogs[].theme.showAvatar` | boolean |  |
| `user.blogs[].theme.showDescription` | boolean |  |
| `user.blogs[].theme.showHeaderImage` | boolean |  |
| `user.blogs[].theme.showTitle` | boolean |  |
| `user.blogs[].theme.titleColor` | string |  |
| `user.blogs[].theme.titleFont` | string |  |
| `user.blogs[].theme.titleFontWeight` | string |  |
| `user.blogs[].themeId` | number |  |
| `user.blogs[].title` | string |  |
| `user.blogs[].totalPosts` | number |  |
| `user.blogs[].tweet` | string |  |
| `user.blogs[].twitterEnabled` | boolean |  |
| `user.blogs[].twitterSend` | boolean |  |
| `user.blogs[].type` | string |  |
| `user.blogs[].updated` | number |  |
| `user.blogs[].url` | string |  |
| `user.blogs[].uuid` | string |  |
| `user.defaultPostFormat` | string |  |
| `user.following` | number |  |
| `user.likes` | number |  |
| `user.name` | string |  |

## Native endpoint

Through the native Tumblr API, this operation is `GET /v2/user/info` (base URL `https://api.tumblr.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-information.md) for the provider-specific parameters and requirements.

