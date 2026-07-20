# <img src="https://images.mindcloud.co/apps/icons/e-gain_1775040355423.png" alt="eGain logo" width="28" height="28"> eGain: Universal API

eGain Conversation Manager APIs for managing authentications, client applications, participants, channels, orchestrations, and accounts through eGain's server-to-server OAuth2 contract.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/eGain/latest
- **Actions:** 35
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.egain.com
- **Vendor API docs:** https://apidev.egain.com/api-catalog/conversation-conversationmgr/api-bundled/overview/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Authentications](actions/list-authentications.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eGain/latest/actions/list-authentications?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (35)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Create Account](actions/create-account.md) | POST | Creates a new account in eGain. |
| [Delete Account](actions/delete-account.md) | DELETE | Deletes an existing account from eGain. |
| [Get Account](actions/get-account.md) | GET | Retrieves an account from eGain. |
| [List Accounts](actions/list-accounts.md) | GET | Retrieves a list of accounts from eGain. |
| [Update Account](actions/update-account.md) | PUT | Updates an existing account in eGain. |

### Asset

| Action | Method | Description |
| --- | --- | --- |
| [Create Asset](actions/create-asset.md) | POST | Creates an asset upload URL in eGain. |
| [Delete Asset](actions/delete-asset.md) | DELETE | Deletes an existing asset from eGain. |
| [Get Asset](actions/get-asset.md) | GET | Retrieves an asset download URL from eGain. |

### Authentication

| Action | Method | Description |
| --- | --- | --- |
| [Create Authentication](actions/create-authentication.md) | POST | Creates a new authentication in eGain. |
| [Delete Authentication](actions/delete-authentication.md) | DELETE | Deletes an existing authentication from eGain. |
| [Get Authentication](actions/get-authentication.md) | GET | Retrieves an authentication from eGain. |
| [List Authentications](actions/list-authentications.md) | GET | Retrieves a list of authentications from eGain. |
| [Update Authentication](actions/update-authentication.md) | PUT | Updates an existing authentication in eGain. |

### Channel

| Action | Method | Description |
| --- | --- | --- |
| [Create Channel](actions/create-channel.md) | POST | Creates a new channel in eGain. |
| [Delete Channel](actions/delete-channel.md) | DELETE | Deletes an existing channel from eGain. |
| [Get Channel](actions/get-channel.md) | GET | Retrieves a channel from eGain. |
| [List Channels](actions/list-channels.md) | GET | Retrieves a list of channels from eGain. |
| [Update Channel](actions/update-channel.md) | PUT | Updates an existing channel in eGain. |

### Client Application

| Action | Method | Description |
| --- | --- | --- |
| [Create Client Application](actions/create-client-application.md) | POST | Creates a new client application in eGain. |
| [Delete Client Application](actions/delete-client-application.md) | DELETE | Deletes an existing client application from eGain. |
| [Get Client Application](actions/get-client-application.md) | GET | Retrieves a client application from eGain. |
| [List Client Applications](actions/list-client-applications.md) | GET | Retrieves a list of client applications from eGain. |
| [Update Client Application](actions/update-client-application.md) | PUT | Updates an existing client application in eGain. |

### Conversation

| Action | Method | Description |
| --- | --- | --- |
| [Get Conversation](actions/get-conversation.md) | GET | Retrieves a conversation from eGain. |

### Conversation Message

| Action | Method | Description |
| --- | --- | --- |
| [Send Message](actions/send-message.md) | POST | Sends conversation messages in eGain Conversation Hub. |

### Orchestration

| Action | Method | Description |
| --- | --- | --- |
| [Create Orchestration](actions/create-orchestration.md) | POST | Creates a new orchestration in eGain. |
| [Delete Orchestration](actions/delete-orchestration.md) | DELETE | Deletes an existing orchestration from eGain. |
| [Get Orchestration](actions/get-orchestration.md) | GET | Retrieves an orchestration from eGain. |
| [List Orchestrations](actions/list-orchestrations.md) | GET | Retrieves a list of orchestrations from eGain. |
| [Update Orchestration](actions/update-orchestration.md) | PUT | Updates an existing orchestration in eGain. |

### Participant

| Action | Method | Description |
| --- | --- | --- |
| [Create Participant](actions/create-participant.md) | POST | Creates a new participant in eGain. |
| [Delete Participant](actions/delete-participant.md) | DELETE | Deletes an existing participant from eGain. |
| [Get Participant](actions/get-participant.md) | GET | Retrieves a participant from eGain. |
| [List Participants](actions/list-participants.md) | GET | Retrieves a list of participants from eGain. |
| [Update Participant](actions/update-participant.md) | PUT | Updates an existing participant in eGain. |

