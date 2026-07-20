# <img src="https://images.mindcloud.co/apps/icons/chat-bot_1782742282032.png" alt="ChatBot logo" width="28" height="28"> ChatBot: Universal API

Manage ChatBot stories, users, training, and conversation data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/chatBot/latest
- **Category:** Marketing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.chatbot.com
- **Vendor API docs:** https://www.chatbot.com/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Stories](actions/list-stories.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatBot/latest/actions/list-stories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Chat

| Action | Method | Description |
| --- | --- | --- |
| [Get Chat](actions/get-chat.md) | GET | Retrieves chat details from ChatBot API. |
| [List Chats](actions/list-chats.md) | GET | Retrieves chat records from ChatBot API. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Conversations Report](actions/get-conversations-report.md) | GET | Retrieves conversations report data from ChatBot API. |

### Segment

| Action | Method | Description |
| --- | --- | --- |
| [Create Segment](actions/create-segment.md) | POST | Creates a new user segment in ChatBot. |
| [List Segments](actions/list-segments.md) | GET | Retrieves segment records from ChatBot API. |

### Story

| Action | Method | Description |
| --- | --- | --- |
| [Create Story](actions/create-story.md) | POST | Creates a new story in ChatBot API. |
| [Get Story](actions/get-story.md) | GET | Retrieves chatbot story details from ChatBot API. |
| [List Stories](actions/list-stories.md) | GET | Retrieves chatbot story records from ChatBot API. |
| [Update Story](actions/update-story.md) | PUT | Updates an existing story in ChatBot API. |

### Training Phrase

| Action | Method | Description |
| --- | --- | --- |
| [List Phrases](actions/list-phrases.md) | GET | Retrieves training phrase records from ChatBot API. |
| [Train Phrases](actions/train-phrases.md) | PUT | Trains existing phrases in the ChatBot model. |
| [Train with Custom Text](actions/train-with-custom-text.md) | PUT | Trains ChatBot with custom text input. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Add segments to User](actions/add-segments-to-user.md) | PUT | Adds segments to an existing ChatBot user. |
| [Ban or Unban User](actions/ban-or-unban-user.md) | PUT | Updates the ban status of a ChatBot user. |
| [Create User](actions/create-user.md) | POST | Creates a new user in ChatBot API. |
| [Export Users](actions/export-users.md) | GET | Exports user records from ChatBot API. |
| [Get User](actions/get-user.md) | GET | Retrieves user details from ChatBot API. |
| [List Users](actions/list-users.md) | GET | Retrieves user records from ChatBot API. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in ChatBot API. |
| [Update User Segments](actions/update-user-segments.md) | PUT | Updates segments for an existing ChatBot user. |

### User Entity

| Action | Method | Description |
| --- | --- | --- |
| [Create User Entity](actions/create-user-entity.md) | POST | Creates a new user entity in ChatBot. |
| [Get User Entity](actions/get-user-entity.md) | GET | Retrieves user entity details from ChatBot API. |
| [List User Entities](actions/list-user-entities.md) | GET | Retrieves user entity records from ChatBot API. |
| [Update User Entity](actions/update-user-entity.md) | PUT | Updates an existing user entity in ChatBot. |

