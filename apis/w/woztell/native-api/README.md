# Woztell: Native API Reference

A consolidated summary of Woztell's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://doc.woztell.com/open-api-reference/
- **API base URL:** `https://open.api.woztell.com/v3`

## Authentication

### Access Token

Connect with a user-generated Woztell access token.

### Credentials

- **API Key:** `apiKey` · required
- **Channel ID:** `channelId` · optional · Optional default Woztell channel ID for channel-scoped actions.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.woztell.com/portal/en/kb/articles/access-token)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data.apiViewer.app`.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Audience](actions/create-audience.md) | `POST /` | [docs](https://doc.woztell.com/open-api-reference/#mutation-createAudience) |
| [Create Broadcast](actions/create-broadcast.md) | `POST /` | [docs](https://doc.woztell.com/open-api-reference/#mutation-createBroadcast) |
| [Create Channel](actions/create-channel.md) | `POST /` | [docs](https://doc.woztell.com/open-api-reference/#mutation-createChannel) |
| [Create Tree](actions/create-tree.md) | `POST /` | [docs](https://doc.woztell.com/open-api-reference/#mutation-createTree) |
| [Get App Info](actions/get-app-info.md) | `POST /` | [docs](https://doc.woztell.com/open-api-reference/#query-apiViewer) |
| [Get Background Task](actions/get-background-task.md) | `POST /` | [docs](https://doc.woztell.com/docs/reference/open-api-reference/) |
| [Get Chat](actions/get-chat.md) | `POST /` | [docs](https://doc.woztell.com/docs/reference/open-api-reference/) |
| [Get File](actions/get-file.md) | `POST /` | [docs](https://doc.woztell.com/docs/reference/open-api-reference/) |
| [Get Installed Integration](actions/get-installed-integration.md) | `POST /` | [docs](https://doc.woztell.com/docs/reference/open-api-reference/) |
| [Get Member](actions/get-member.md) | `POST /` | [docs](https://doc.woztell.com/docs/reference/open-api-reference/) |
| [Get Ticket](actions/get-ticket.md) | `POST /` | [docs](https://doc.woztell.com/open-api-reference/#query-apiViewer) |
| [Get Tree](actions/get-tree.md) | `POST /` | [docs](https://doc.woztell.com/open-api-reference/#query-apiViewer) |
| [List Actions](actions/list-actions.md) | `POST /` | [docs](https://doc.woztell.com/docs/reference/open-api-reference/) |
| [List App Integrations](actions/list-app-integrations.md) | `POST /` | [docs](https://doc.woztell.com/docs/reference/open-api-reference/) |
| [List Audiences](actions/list-audiences.md) | `POST /` | [docs](https://doc.woztell.com/open-api-reference/#query-apiViewer) |
| [List Channels](actions/list-channels.md) | `POST /` | [docs](https://doc.woztell.com/open-api-reference/#query-apiViewer) |
| [List Conversation History](actions/list-conversation-history.md) | `POST /` | [docs](https://doc.woztell.com/open-api-reference/#query-apiViewer) |
| [List Files](actions/list-files.md) | `POST /` | [docs](https://doc.woztell.com/open-api-reference/#query-apiViewer) |
| [List Installed Integrations](actions/list-installed-integrations.md) | `POST /` | [docs](https://doc.woztell.com/docs/reference/open-api-reference/) |
| [List Locale Groups](actions/list-locale-groups.md) | `POST /` | [docs](https://doc.woztell.com/docs/reference/open-api-reference/) |
| [List Nodes](actions/list-nodes.md) | `POST /` | [docs](https://doc.woztell.com/docs/reference/open-api-reference/) |
| [List Priority Groups](actions/list-priority-groups.md) | `POST /` | [docs](https://doc.woztell.com/docs/reference/open-api-reference/) |
| [List Responses](actions/list-responses.md) | `POST /` | [docs](https://doc.woztell.com/docs/reference/open-api-reference/) |
| [List Subscription Pushes](actions/list-subscription-pushes.md) | `POST /` | [docs](https://doc.woztell.com/open-api-reference/#query-apiViewer) |
| [List Tickets](actions/list-tickets.md) | `POST /` | [docs](https://doc.woztell.com/open-api-reference/#query-apiViewer) |
| [List Trees](actions/list-trees.md) | `POST /` | [docs](https://doc.woztell.com/open-api-reference/#query-apiViewer) |
| [List Triggers](actions/list-triggers.md) | `POST /` | [docs](https://doc.woztell.com/docs/reference/open-api-reference/) |
| [Search Members](actions/search-members.md) | `POST /` | [docs](https://doc.woztell.com/open-api-reference/#query-apiViewer) |
| [Update Audience](actions/update-audience.md) | `POST /` | [docs](https://doc.woztell.com/open-api-reference/#mutation-updateAudience) |
| [Update Tree](actions/update-tree.md) | `POST /` | [docs](https://doc.woztell.com/open-api-reference/#mutation-updateTree) |
