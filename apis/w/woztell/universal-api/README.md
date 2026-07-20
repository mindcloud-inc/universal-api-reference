# <img src="https://images.mindcloud.co/apps/icons/id-bp9m1os-u-1773858796640_1773858801820.jpeg" alt="Woztell logo" width="28" height="28"> Woztell: Universal API

Manage Woztell channels, members, and chatbot conversations

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/woztell/latest
- **Category:** Communication / Team Messaging
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://woztell.com
- **Vendor API docs:** https://doc.woztell.com/open-api-reference/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get App Info](actions/get-app-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/woztell/latest/actions/get-app-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Actions

| Action | Method | Description |
| --- | --- | --- |
| [List Actions](actions/list-actions.md) | GET | Retrieves actions from your Woztell workspace. |

### App

| Action | Method | Description |
| --- | --- | --- |
| [Get App Info](actions/get-app-info.md) | GET | Retrieves app information from your Woztell workspace. |

### Audience

| Action | Method | Description |
| --- | --- | --- |
| [Create Audience](actions/create-audience.md) | POST | Creates an audience in your Woztell workspace. |
| [List Audiences](actions/list-audiences.md) | GET | Retrieves audiences from your Woztell workspace. |
| [Update Audience](actions/update-audience.md) | PUT | Updates an audience in your Woztell workspace. |

### Channel

| Action | Method | Description |
| --- | --- | --- |
| [Create Channel](actions/create-channel.md) | POST | Creates a channel in your Woztell workspace. |
| [List Channels](actions/list-channels.md) | GET | Retrieves channels from your Woztell workspace. |

### Chat

| Action | Method | Description |
| --- | --- | --- |
| [List Conversation History](actions/list-conversation-history.md) | GET | Retrieves conversation history from your Woztell workspace. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [List Files](actions/list-files.md) | GET | Retrieves files from your Woztell workspace. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Get File](actions/get-file.md) | GET | Retrieves a file from your Woztell workspace. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [List Locale Groups](actions/list-locale-groups.md) | GET | Retrieves locale groups from your Woztell workspace. |
| [List Priority Groups](actions/list-priority-groups.md) | GET | Retrieves priority groups from your Woztell workspace. |

### Integrations

| Action | Method | Description |
| --- | --- | --- |
| [Get Installed Integration](actions/get-installed-integration.md) | GET | Retrieves an installed integration from your Woztell workspace. |
| [List App Integrations](actions/list-app-integrations.md) | GET | Retrieves app integrations from your Woztell workspace. |
| [List Installed Integrations](actions/list-installed-integrations.md) | GET | Retrieves installed integrations from your Woztell workspace. |

### Member

| Action | Method | Description |
| --- | --- | --- |
| [Search Members](actions/search-members.md) | GET | Finds members in your Woztell workspace. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Get Chat](actions/get-chat.md) | GET | Retrieves a chat from your Woztell workspace. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [List Nodes](actions/list-nodes.md) | GET | Retrieves nodes from your Woztell workspace. |

### Subscribers

| Action | Method | Description |
| --- | --- | --- |
| [Get Member](actions/get-member.md) | GET | Retrieves a member from your Woztell workspace. |

### Subscriptionpush

| Action | Method | Description |
| --- | --- | --- |
| [Create Broadcast](actions/create-broadcast.md) | POST | Creates a broadcast in your Woztell workspace. |
| [List Subscription Pushes](actions/list-subscription-pushes.md) | GET | Retrieves subscription pushes from your Woztell workspace. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Get Background Task](actions/get-background-task.md) | GET | Retrieves a background task from your Woztell workspace. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [List Responses](actions/list-responses.md) | GET | Retrieves responses from your Woztell workspace. |

### Ticket

| Action | Method | Description |
| --- | --- | --- |
| [Get Ticket](actions/get-ticket.md) | GET | Retrieves a ticket from your Woztell workspace. |
| [List Tickets](actions/list-tickets.md) | GET | Retrieves tickets from your Woztell workspace. |

### Tree

| Action | Method | Description |
| --- | --- | --- |
| [Create Tree](actions/create-tree.md) | POST | Creates a tree in your Woztell workspace. |
| [Get Tree](actions/get-tree.md) | GET | Retrieves a tree from your Woztell workspace. |
| [List Trees](actions/list-trees.md) | GET | Retrieves trees from your Woztell workspace. |
| [Update Tree](actions/update-tree.md) | PUT | Updates a tree in your Woztell workspace. |

### Triggers

| Action | Method | Description |
| --- | --- | --- |
| [List Triggers](actions/list-triggers.md) | GET | Retrieves triggers from your Woztell workspace. |

