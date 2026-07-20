# Tumblr: Reblog Post (NPF)

Reblogs a Tumblr post using NPF.

```
POST https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/reblog-post-npf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tumblr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/reblog-post-npf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "blogIdentifier": "mindcloudapps",
  "parentTumblelogUuid": "t:D0BHH6KaTIoQrDUlPnShDA",
  "parentPostId": "1772822948",
  "reblogKey": "reblog-key-from-source-post"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/reblog-post-npf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "blogIdentifier": "mindcloudapps",
    "parentTumblelogUuid": "t:D0BHH6KaTIoQrDUlPnShDA",
    "parentPostId": "1772822948",
    "reblogKey": "reblog-key-from-source-post"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `blogIdentifier` | string | yes | Any Tumblr blog identifier for the target blog. Example: `mindcloudapps`. |
| `parentTumblelogUuid` | string | yes | UUID of the blog being reblogged from. Example: `t:D0BHH6KaTIoQrDUlPnShDA`. |
| `parentPostId` | string | yes | ID of the post being reblogged. Example: `1772822948`. |
| `reblogKey` | string | yes | Reblog key validating the reblog action. Example: `reblog-key-from-source-post`. |
| `content[]` | array<object> | no | Optional NPF content blocks to add to the end of the reblog trail. Example: `[object Object]`. |
| `state` | list<string> | no | Initial state for the new reblog post. One of: `draft`, `private`, `published`, `queue`, `unapproved`. Default: `published`. |
| `tags` | string | no | Comma-separated list of tags to associate with the reblog. Example: `mindcloud,tumblr`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `layout[]` | array<object> | no | Optional NPF layout objects for arranging added content blocks. Example: `[object Object]`. |
| `hideTrail` | boolean | no | Whether to hide the full reblog trail in the new reblog. |
| `excludeTrailItems[]` | array<number> | no | Specific reblog trail item indexes to exclude from the new reblog. Example: `0`. |
| `publishOn` | date | no | Future ISO 8601 date/time to publish a queued reblog. Example: `2026-03-07T15:00:00Z`. |
| `date` | date | no | Past ISO 8601 date/time used to backdate the reblog. Example: `2026-03-01T15:00:00Z`. |
| `slug` | string | no | Custom URL slug to use in the reblog permalink. Example: `reblogged-via-mindcloud`. |
| `sourceUrl` | string | no | Source attribution URL for the reblog content. Example: `https://example.com/source`. |
| `interactabilityReblog` | list<string> | no | Who can interact with this reblog when reblogging. One of: `everyone`, `noone`. |
| `sendToTwitter` | boolean | no | Whether to share the reblog to a connected Twitter account. |
| `isPrivate` | boolean | no | Whether this should be a private answer when reblogging an answer post. |

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

Through the native Tumblr API, this operation is `POST /v2/blog/:blogIdentifier/posts` (base URL `https://api.tumblr.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reblog-post-npf.md) for the provider-specific parameters and requirements.

