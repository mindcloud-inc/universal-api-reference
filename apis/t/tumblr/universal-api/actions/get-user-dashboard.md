# Tumblr: Get User Dashboard

Retrieves the authenticated user's Tumblr dashboard.

```
GET https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/get-user-dashboard
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tumblr `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/get-user-dashboard?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/get-user-dashboard?${params}`, {
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
| `type` | list<string> | no | Post type to return. One of: `answer`, `audio`, `chat`, `link`, `photo`, `quote`, `text`, `video`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sinceId` | string | no | Return posts that have appeared after this ID. |
| `reblogInfo` | boolean | no | Return reblog information. |
| `notesInfo` | boolean | no | Return note count and note metadata. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "posts": [
        {
          "blog": {
            "avatar": [
              {
                "height": 1,
                "url": "https://example.com",
                "width": 1
              }
            ],
            "canShowBadges": true,
            "description": "string",
            "name": "Ava Chen",
            "title": "string",
            "updated": 1,
            "url": "https://example.com",
            "uuid": "string"
          },
          "blogName": "Ava Chen",
          "canBlaze": true,
          "canIgnite": true,
          "canLike": true,
          "canMute": true,
          "canReblog": true,
          "canReply": true,
          "canSendInMessage": true,
          "content": [
            {
              "subtype": "string",
              "text": "string",
              "type": "string"
            }
          ],
          "date": "string",
          "displayAvatar": true,
          "followed": true,
          "id": 1,
          "idString": "string",
          "interactabilityBlaze": "string",
          "interactabilityReblog": "string",
          "isBlazed": true,
          "isBlazePending": true,
          "isBlocksPostFormat": true,
          "liked": true,
          "muted": true,
          "muteEndTimestamp": 1,
          "noteCount": 1,
          "originalType": "string",
          "postUrl": "https://example.com",
          "reblogKey": "string",
          "recommendedColor": {},
          "recommendedSource": {},
          "shortUrl": "https://example.com",
          "shouldOpenInLegacy": true,
          "slug": "string",
          "state": "string",
          "summary": "string",
          "timestamp": 1,
          "type": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `posts[].blog.avatar[].height` | number |  |
| `posts[].blog.avatar[].url` | string |  |
| `posts[].blog.avatar[].width` | number |  |
| `posts[].blog.canShowBadges` | boolean |  |
| `posts[].blog.description` | string |  |
| `posts[].blog.name` | string |  |
| `posts[].blog.title` | string |  |
| `posts[].blog.updated` | number |  |
| `posts[].blog.url` | string |  |
| `posts[].blog.uuid` | string |  |
| `posts[].blogName` | string |  |
| `posts[].canBlaze` | boolean |  |
| `posts[].canIgnite` | boolean |  |
| `posts[].canLike` | boolean |  |
| `posts[].canMute` | boolean |  |
| `posts[].canReblog` | boolean |  |
| `posts[].canReply` | boolean |  |
| `posts[].canSendInMessage` | boolean |  |
| `posts[].content[].subtype` | string |  |
| `posts[].content[].text` | string |  |
| `posts[].content[].type` | string |  |
| `posts[].date` | string |  |
| `posts[].displayAvatar` | boolean |  |
| `posts[].followed` | boolean |  |
| `posts[].id` | number |  |
| `posts[].idString` | string |  |
| `posts[].interactabilityBlaze` | string |  |
| `posts[].interactabilityReblog` | string |  |
| `posts[].isBlazed` | boolean |  |
| `posts[].isBlazePending` | boolean |  |
| `posts[].isBlocksPostFormat` | boolean |  |
| `posts[].liked` | boolean |  |
| `posts[].muted` | boolean |  |
| `posts[].muteEndTimestamp` | number |  |
| `posts[].noteCount` | number |  |
| `posts[].originalType` | string |  |
| `posts[].postUrl` | string |  |
| `posts[].reblogKey` | string |  |
| `posts[].recommendedColor` | object |  |
| `posts[].recommendedSource` | object |  |
| `posts[].shortUrl` | string |  |
| `posts[].shouldOpenInLegacy` | boolean |  |
| `posts[].slug` | string |  |
| `posts[].state` | string |  |
| `posts[].summary` | string |  |
| `posts[].timestamp` | number |  |
| `posts[].type` | string |  |

## Native endpoint

Through the native Tumblr API, this operation is `GET /v2/user/dashboard` (base URL `https://api.tumblr.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-user-dashboard.md) for the provider-specific parameters and requirements.

