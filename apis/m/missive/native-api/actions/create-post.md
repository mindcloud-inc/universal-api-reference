# Create Post with Missive

Creates a post in your Missive workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/posts`
- **Base URL:** `https://public.missiveapp.com/v1`
- **Official documentation:** [Create Post](https://missiveapp.com/docs/developers/rest-api/endpoints#create-a-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `posts` | body | `object` | no | Top-level post object required by the Missive posts endpoint. |
| `posts.username` | body | `string` | no | Name of the post author used instead of the API token owner's name. |
| `posts.username_icon` | body | `string` | no | Image URL of the post author used instead of the API token owner's avatar. |
| `posts.conversation_icon` | body | `string` | no | Image URL used as the icon in the conversation list. |
| `posts.conversation_subject` | body | `string` | no | Subject for a new conversation created by the post. |
| `posts.conversation_color` | body | `string` | no | Conversation color as a HEX code or one of good, warning, or danger. |
| `posts.text` | body | `string` | no | Main message of a post as plain text. |
| `posts.markdown` | body | `string` | no | Main message of a post formatted with Markdown. |
| `posts.notification` | body | `object` | yes | Notification object with title and body keys used to render a notification. |
| `posts.attachments[]` | body | `array<object>` | no | Array of attachment objects for the post. |
| `posts.references[]` | body | `array<string>` | no | References used to append the post to an existing conversation. |
| `posts.conversation` | body | `string` | no | Conversation ID to append the post to an existing conversation. |
| `posts.organization` | body | `string` | no | Organization ID used to scope or link the conversation. |
| `posts.team` | body | `string` | no | Team ID used to link the conversation to a team. |
| `posts.force_team` | body | `boolean` | no | Pass true to force a new team even if the conversation is already in another team. |
| `posts.add_users[]` | body | `array<string>` | no | User IDs that should get access to the conversation. Requires Organization when provided. |
| `posts.add_assignees[]` | body | `array<string>` | no | User IDs to assign to the conversation. Requires Organization when provided. |
| `posts.add_shared_labels[]` | body | `array<string>` | no | Shared label IDs to add to the conversation. |
| `posts.remove_shared_labels[]` | body | `array<string>` | no | Shared label IDs to remove from the conversation. |
| `posts.add_to_inbox` | body | `boolean` | no | Pass true to move the conversation to Inbox for everyone with access. |
| `posts.add_to_team_inbox` | body | `boolean` | no | Pass true to move the conversation to a team inbox. Requires Team when provided. |
| `posts.close` | body | `boolean` | no | Pass true to close the conversation for everyone with access. |
| `posts.reopen` | body | `boolean` | no | Pass true to keep a closed conversation closed after adding the post. |
