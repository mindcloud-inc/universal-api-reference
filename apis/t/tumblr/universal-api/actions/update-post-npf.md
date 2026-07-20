# Tumblr: Update Post (NPF)

Updates an existing Tumblr post using NPF.

```
PUT https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/update-post-npf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tumblr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/update-post-npf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "blogIdentifier": "mindcloudapps",
  "postId": "1772822948"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/update-post-npf', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "blogIdentifier": "mindcloudapps",
    "postId": "1772822948"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `blogIdentifier` | string | yes | Any Tumblr blog identifier for the target blog. Example: `mindcloudapps`. |
| `postId` | string | yes | ID of the post to edit. Example: `1772822948`. |
| `content[]` | array<object> | no | NPF content blocks for the edited post. Example: `[object Object]`. |
| `state` | list<string> | no | Updated state for the post. One of: `draft`, `private`, `published`, `queue`, `unapproved`. |
| `tags` | string | no | Comma-separated list of tags to associate with the post. Example: `mindcloud,tumblr`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `layout[]` | array<object> | no | Optional NPF layout objects for arranging the content blocks. Example: `[object Object]`. |
| `publishOn` | date | no | Future ISO 8601 date/time to publish a queued post. Example: `2026-03-07T15:00:00Z`. |
| `date` | date | no | Past ISO 8601 date/time used to backdate the post. Example: `2026-03-01T15:00:00Z`. |
| `slug` | string | no | Custom URL slug to use in the post permalink. Example: `updated-via-mindcloud`. |
| `sourceUrl` | string | no | Source attribution URL for the post content. Example: `https://example.com/source`. |
| `interactabilityReblog` | list<string> | no | Who can interact with this post when reblogging. One of: `everyone`, `noone`. |
| `sendToTwitter` | boolean | no | Whether to share the edited post to a connected Twitter account. |
| `isPrivate` | boolean | no | Whether this should be a private answer when editing an answer post. |
| `parentTumblelogUuid` | string | no | UUID of the reblog source blog when editing a reblog. Example: `t:D0BHH6KaTIoQrDUlPnShDA`. |
| `parentPostId` | string | no | ID of the reblog source post when editing a reblog. Example: `1772822948`. |
| `reblogKey` | string | no | Reblog key for the reblog source post when editing a reblog. Example: `reblog-key-from-source-post`. |
| `hideTrail` | boolean | no | Whether to hide the full reblog trail in the edited reblog. |
| `excludeTrailItems[]` | array<number> | no | Specific reblog trail item indexes to exclude when editing a reblog. Example: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "displayText": "string",
      "id": "string",
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `displayText` | string |  |
| `id` | string |  |
| `state` | string |  |

## Native endpoint

Through the native Tumblr API, this operation is `PUT /v2/blog/:blogIdentifier/posts/:postId` (base URL `https://api.tumblr.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-post-npf.md) for the provider-specific parameters and requirements.

