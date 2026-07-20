# <img src="https://images.mindcloud.co/apps/icons/logo_1775645339187.jpeg" alt="Chaindesk logo" width="28" height="28"> Chaindesk: Universal API

Manage AI agents, knowledge bases, and support conversations

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/chaindesk/latest
- **Category:** Support / Ticketing
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.chaindesk.ai
- **Vendor API docs:** https://docs.chaindesk.ai/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Conversations](actions/list-conversations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/list-conversations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Agent

| Action | Method | Description |
| --- | --- | --- |
| [Create Agent](actions/create-agent.md) | POST | Creates a new agent in Chaindesk. |
| [Delete Agent](actions/delete-agent.md) | DELETE | Deletes an existing agent from Chaindesk. |
| [Get Agent](actions/get-agent.md) | GET | Retrieves an existing agent from Chaindesk. |
| [List Agents](actions/list-agents.md) | GET | Retrieves agents from your Chaindesk workspace. |
| [Update Agent](actions/update-agent.md) | PUT | Updates an existing agent in Chaindesk. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Chaindesk. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from your Chaindesk workspace. |

### Conversations

| Action | Method | Description |
| --- | --- | --- |
| [List Agent Conversations](actions/list-agent-conversations.md) | GET | Retrieves conversations for an agent in Chaindesk. |
| [List Conversations](actions/list-conversations.md) | GET | Retrieves conversations from your Chaindesk workspace. |

### Data Sources

| Action | Method | Description |
| --- | --- | --- |
| [Create Text Datasource](actions/create-text-datasource.md) | POST | Creates a text datasource in Chaindesk. |
| [Create Web Page Datasource](actions/create-web-page-datasource.md) | POST | Creates a web page datasource in Chaindesk. |
| [Get Datasource](actions/get-datasource.md) | GET | Retrieves an existing datasource from Chaindesk. |
| [List Datasources](actions/list-datasources.md) | GET | Retrieves datasources from your Chaindesk workspace. |
| [List Datastore Datasources](actions/list-datastore-datasources.md) | GET | Retrieves datasources for a datastore in Chaindesk. |

### Datastore

| Action | Method | Description |
| --- | --- | --- |
| [Create Pinecone Datastore](actions/create-pinecone-datastore.md) | POST | Creates a Pinecone datastore in Chaindesk. |
| [Create Qdrant Datastore](actions/create-qdrant-datastore.md) | POST | Creates a Qdrant datastore in Chaindesk. |
| [Create S3 Datastore](actions/create-s3-datastore.md) | POST | Creates an S3 datastore in Chaindesk. |
| [Delete Datastore](actions/delete-datastore.md) | DELETE | Deletes an existing datastore from Chaindesk. |
| [Get Datastore](actions/get-datastore.md) | GET | Retrieves an existing datastore from Chaindesk. |
| [List Datastores](actions/list-datastores.md) | GET | Retrieves datastores from your Chaindesk workspace. |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [Create Form](actions/create-form.md) | POST | Creates a new form in Chaindesk. |
| [List Forms](actions/list-forms.md) | GET | Retrieves forms from your Chaindesk workspace. |

### Mail Inbox

| Action | Method | Description |
| --- | --- | --- |
| [Create Mail Inbox](actions/create-mail-inbox.md) | POST | Creates a mail inbox in Chaindesk. |
| [Delete Mail Inbox](actions/delete-mail-inbox.md) | DELETE | Deletes a mail inbox from Chaindesk. |
| [Get Mail Inbox](actions/get-mail-inbox.md) | GET | Retrieves a mail inbox from Chaindesk. |
| [List Mail Inboxes](actions/list-mail-inboxes.md) | GET | Retrieves mail inboxes from your Chaindesk workspace. |
| [Update Mail Inbox](actions/update-mail-inbox.md) | PUT | Updates a mail inbox in Chaindesk. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Continue Agent Conversation](actions/continue-agent-conversation.md) | POST | Sends a follow-up query in a Chaindesk conversation. |
| [Get Conversation Messages](actions/get-conversation-messages.md) | GET | Retrieves messages from a Chaindesk conversation. |
| [Query Agent](actions/query-agent.md) | POST | Sends a query to an agent in Chaindesk. |

