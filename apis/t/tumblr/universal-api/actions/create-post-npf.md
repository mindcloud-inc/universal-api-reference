# Tumblr: Create Post (NPF)

Creates a new Tumblr post using NPF.

```
POST https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/create-post-npf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tumblr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/create-post-npf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "blogIdentifier": "mindcloudapps",
  "content[]": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/create-post-npf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "blogIdentifier": "mindcloudapps",
    "content[]": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `blogIdentifier` | string | yes | Any Tumblr blog identifier for the target blog. Example: `mindcloudapps`. |
| `content[]` | array<object> | yes | NPF content blocks to include in the post. Example: `[object Object]`. |
| `state` | list<string> | no | Initial state for the new post. One of: `draft`, `private`, `published`, `queue`, `unapproved`. Default: `published`. |
| `tags` | string | no | Comma-separated list of tags to associate with the post. Example: `mindcloud,tumblr`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `layout[]` | array<object> | no | Optional NPF layout objects for arranging the content blocks. Example: `[object Object]`. |
| `publishOn` | date | no | Future ISO 8601 date/time to publish a queued post. Example: `2026-03-07T15:00:00Z`. |
| `date` | date | no | Past ISO 8601 date/time used to backdate the post. Example: `2026-03-01T15:00:00Z`. |
| `slug` | string | no | Custom URL slug to use in the post permalink. Example: `hello-from-mindcloud`. |
| `sourceUrl` | string | no | Source attribution URL for the post content. Example: `https://example.com/source`. |
| `interactabilityReblog` | list<string> | no | Who can interact with this post when reblogging. One of: `everyone`, `noone`. |
| `sendToTwitter` | boolean | no | Whether to share the post to a connected Twitter account. |
| `isPrivate` | boolean | no | Whether this should be a private answer when creating an answer post. |

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

Through the native Tumblr API, this operation is `POST /v2/blog/:blogIdentifier/posts` (base URL `https://api.tumblr.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-post-npf.md) for the provider-specific parameters and requirements.

