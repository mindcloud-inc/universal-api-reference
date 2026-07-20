# Tumblr: Get Post (NPF)

Retrieves a Tumblr post using NPF.

```
GET https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/get-post-npf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tumblr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/get-post-npf?connectionId=$CONNECTION_ID&blogIdentifier=string&postId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "blogIdentifier": "string",
  "postId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/get-post-npf?${params}`, {
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
| `postId` | string | yes | The post ID to fetch. |

## Response

```json
{
  "success": true,
  "data": [
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
      "canSendInMessage": true,
      "content": [
        {
          "subtype": "string",
          "text": "string",
          "type": "string"
        }
      ],
      "date": "string",
      "followed": true,
      "id": "string",
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
      "objectType": "string",
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
      "tumblelogUuid": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blog.avatar[].height` | number |  |
| `blog.avatar[].url` | string |  |
| `blog.avatar[].width` | number |  |
| `blog.canShowBadges` | boolean |  |
| `blog.description` | string |  |
| `blog.name` | string |  |
| `blog.title` | string |  |
| `blog.updated` | number |  |
| `blog.url` | string |  |
| `blog.uuid` | string |  |
| `blogName` | string |  |
| `canBlaze` | boolean |  |
| `canIgnite` | boolean |  |
| `canLike` | boolean |  |
| `canMute` | boolean |  |
| `canReblog` | boolean |  |
| `canSendInMessage` | boolean |  |
| `content[].subtype` | string |  |
| `content[].text` | string |  |
| `content[].type` | string |  |
| `date` | string |  |
| `followed` | boolean |  |
| `id` | string |  |
| `idString` | string |  |
| `interactabilityBlaze` | string |  |
| `interactabilityReblog` | string |  |
| `isBlazed` | boolean |  |
| `isBlazePending` | boolean |  |
| `isBlocksPostFormat` | boolean |  |
| `liked` | boolean |  |
| `muted` | boolean |  |
| `muteEndTimestamp` | number |  |
| `noteCount` | number |  |
| `objectType` | string |  |
| `originalType` | string |  |
| `postUrl` | string |  |
| `reblogKey` | string |  |
| `recommendedColor` | object |  |
| `recommendedSource` | object |  |
| `shortUrl` | string |  |
| `shouldOpenInLegacy` | boolean |  |
| `slug` | string |  |
| `state` | string |  |
| `summary` | string |  |
| `timestamp` | number |  |
| `tumblelogUuid` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Tumblr API, this operation is `GET /v2/blog/:blogIdentifier/posts/:postId` (base URL `https://api.tumblr.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-post-npf.md) for the provider-specific parameters and requirements.

