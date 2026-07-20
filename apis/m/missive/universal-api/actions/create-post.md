# Missive: Create Post

Creates a post in your Missive workspace.

```
POST https://connect.mindcloud.co/v1/universal/missive/latest/actions/create-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Missive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/missive/latest/actions/create-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "posts.notification": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/missive/latest/actions/create-post', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "posts.notification": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `posts` | object | no | Top-level post object required by the Missive posts endpoint. |
| `posts.username` | string | no | Name of the post author used instead of the API token owner's name. |
| `posts.usernameIcon` | string | no | Image URL of the post author used instead of the API token owner's avatar. |
| `posts.conversationIcon` | string | no | Image URL used as the icon in the conversation list. |
| `posts.conversationSubject` | string | no | Subject for a new conversation created by the post. |
| `posts.conversationColor` | string | no | Conversation color as a HEX code or one of good, warning, or danger. |
| `posts.text` | string | no | Main message of a post as plain text. |
| `posts.markdown` | string | no | Main message of a post formatted with Markdown. |
| `posts.notification` | object | yes | Notification object with title and body keys used to render a notification. |
| `posts.attachments[]` | array<object> | no | Array of attachment objects for the post. |
| `posts.references[]` | array<string> | no | References used to append the post to an existing conversation. |
| `posts.conversation` | string | no | Conversation ID to append the post to an existing conversation. |
| `posts.organization` | string | no | Organization ID used to scope or link the conversation. |
| `posts.team` | string | no | Team ID used to link the conversation to a team. |
| `posts.forceTeam` | boolean | no | Pass true to force a new team even if the conversation is already in another team. |
| `posts.addUsers[]` | array<string> | no | User IDs that should get access to the conversation. Requires Organization when provided. |
| `posts.addAssignees[]` | array<string> | no | User IDs to assign to the conversation. Requires Organization when provided. |
| `posts.addSharedLabels[]` | array<string> | no | Shared label IDs to add to the conversation. |
| `posts.removeSharedLabels[]` | array<string> | no | Shared label IDs to remove from the conversation. |
| `posts.addToInbox` | boolean | no | Pass true to move the conversation to Inbox for everyone with access. |
| `posts.addToTeamInbox` | boolean | no | Pass true to move the conversation to a team inbox. Requires Team when provided. |
| `posts.close` | boolean | no | Pass true to close the conversation for everyone with access. |
| `posts.reopen` | boolean | no | Pass true to keep a closed conversation closed after adding the post. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conversation": "string",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conversation` | string |  |
| `id` | string |  |

## Native endpoint

Through the native Missive API, this operation is `POST /posts` (base URL `https://public.missiveapp.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-post.md) for the provider-specific parameters and requirements.

