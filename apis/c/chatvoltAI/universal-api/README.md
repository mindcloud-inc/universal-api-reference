# <img src="https://images.mindcloud.co/apps/icons/chatvolt-ai-icon-source_1776085990157.png" alt="Chatvolt AI logo" width="28" height="28"> Chatvolt AI: Universal API

Manage Chatvolt agents, conversations, contacts, dispatches, datastores, artifacts, CRM workflows, and messaging endpoints through the official Chatvolt API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/chatvoltAI/latest
- **Category:** Support / Ticketing
- **Actions:** 107
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://chatvolt.ai
- **Vendor API docs:** https://docs.chatvolt.ai/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contacts](actions/contacts-get.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/contacts-get?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (107)

### Actions

| Action | Method | Description |
| --- | --- | --- |
| [Delete Tool](actions/agents-tools-delete.md) | DELETE | Deletes a tool from Chatvolt AI. |
| [Get Tools](actions/agents-tools-get.md) | GET | Retrieves tools from Chatvolt AI. |
| [Update Tool](actions/agents-tools-patch.md) | PUT | Updates a tool in Chatvolt AI. |
| [Create Tool](actions/agents-tools-post.md) | POST | Creates a tool in Chatvolt AI. |

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Create or Update Dispatch](actions/dispatches-create.md) | PUT | Creates a dispatch in Chatvolt AI, or updates an existing one. |
| [Delete Scheduled Dispatch](actions/dispatches-delete.md) | DELETE | Deletes a scheduled Dispatch from Chatvolt AI. |
| [List Dispatches](actions/dispatches-get.md) | GET | Retrieves dispatches from Chatvolt AI. |
| [Populate Dispatch Queue](actions/dispatches-populate-queue.md) | POST | Populates a dispatch queue in Chatvolt AI. |

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [Create Category](actions/artifacts-categories-create.md) | POST | Creates a category in Chatvolt AI. |
| [Delete Category](actions/artifacts-categories-delete.md) | DELETE | Deletes a category from Chatvolt AI. |
| [Get Category](actions/artifacts-categories-get.md) | GET | Retrieves a category from Chatvolt AI. |
| [List Categories](actions/artifacts-categories-list.md) | GET | Retrieves categories from Chatvolt AI. |
| [Update Category](actions/artifacts-categories-update.md) | PUT | Updates a category in Chatvolt AI. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create or Update Contact](actions/contacts-create.md) | PUT | Creates a contact in Chatvolt AI, or updates an existing one. |
| [List Contacts](actions/contacts-get.md) | GET | Retrieves contacts from Chatvolt AI. |
| [Get Contact by ID](actions/dispatches-contacts-get-by-id.md) | GET | Retrieves a contact from Chatvolt AI. |

### Conversations

| Action | Method | Description |
| --- | --- | --- |
| [Assign to User](actions/conversation-assign.md) | PUT | Assigns a conversation to a user in Chatvolt AI. |
| [Delete Conversation](actions/conversation-delete-conversation.md) | DELETE | Deletes a conversation from Chatvolt AI. |
| [Get Conversation By Id](actions/conversation-get-by-id.md) | GET | Retrieves a conversation from Chatvolt AI. |
| [List Conversations by Date](actions/conversation-list-by-date.md) | GET | Retrieves conversations by date from Chatvolt AI. |
| [Enable/Disable AI for Conversation](actions/conversation-set-ai-enabled.md) | PUT | Enables or disables AI for a conversation in Chatvolt AI. |
| [Set Priority](actions/conversation-set-priority.md) | PUT | Sets a conversation priority in Chatvolt AI. |
| [Update Status](actions/conversation-update-status.md) | PUT | Updates a conversation status in Chatvolt AI. |
| [Delete CRM Conversation Log](actions/crm-conversation-log-delete-crm-conversation-log.md) | DELETE | Deletes an existing CRM conversation log from Chatvolt AI. |
| [Get CRM Conversation Log by ID](actions/crm-conversation-log-get-log-by-id.md) | GET | Retrieves a CRM conversation log from Chatvolt AI. |
| [List CRM Conversation Logs](actions/crm-conversation-log-list-crm-conversation-logs.md) | GET | Retrieves CRM conversation logs from Chatvolt AI. |
| [Partially Update CRM Conversation Log](actions/crm-conversation-log-partially-update-crm-conversation-log.md) | PUT | Partially updates a CRM conversation log in Chatvolt AI. |
| [Update CRM Conversation Log](actions/crm-conversation-log-update-crm-conversation-log.md) | PUT | Updates an existing CRM conversation log in Chatvolt AI. |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [Delete Custom Variable](actions/conversation-delete-variable.md) | DELETE | Deletes a custom variable from Chatvolt AI. |
| [Get One Custom Variable](actions/conversation-get-one-variable.md) | GET | Retrieves a custom variable from Chatvolt AI. |
| [Get All Custom Variables](actions/conversation-get-variables.md) | GET | Retrieves custom variables from Chatvolt AI. |
| [Create/Update Custom Variable](actions/conversation-upsert-variable.md) | PUT | Creates a custom variable in Chatvolt AI, or updates an existing one. |

### Data Sources

| Action | Method | Description |
| --- | --- | --- |
| [Create Datasource](actions/datasources-create.md) | POST | Creates a datasource in Chatvolt AI. |
| [Delete Datasource](actions/datasources-delete.md) | DELETE | Deletes a datasource from Chatvolt AI. |
| [Get Datasource](actions/datasources-get.md) | GET | Retrieves a datasource from Chatvolt AI. |
| [List Datasources](actions/datasources-list.md) | GET | Retrieves datasources from Chatvolt AI. |

### Databases

| Action | Method | Description |
| --- | --- | --- |
| [Create Datastore](actions/datastores-create.md) | POST | Creates a datastore in Chatvolt AI. |
| [Delete Datastore](actions/datastores-delete.md) | DELETE | Deletes a datastore from Chatvolt AI. |
| [Get Datastore](actions/datastores-get.md) | GET | Retrieves a datastore from Chatvolt AI. |
| [List Datastores](actions/datastores-list.md) | GET | Retrieves datastores from Chatvolt AI. |
| [Query Datastore](actions/datastores-query.md) | POST | Queries a datastore in Chatvolt AI. |
| [Update Datastore](actions/datastores-update.md) | PUT | Updates a datastore in Chatvolt AI. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Delete Artifacts](actions/artifacts-bulk-delete.md) | DELETE | Deletes artifacts from Chatvolt AI. |
| [Create Artifact](actions/artifacts-create.md) | POST | Creates an artifact in Chatvolt AI. |
| [Delete/Toggle Artifact](actions/artifacts-delete.md) | DELETE | Deletes an artifact from Chatvolt AI, or toggles its active status. |
| [Get Artifact](actions/artifacts-get.md) | GET | Retrieves an artifact from Chatvolt AI. |
| [List Artifacts](actions/artifacts-list.md) | GET | Retrieves artifacts from Chatvolt AI. |
| [Search Artifacts](actions/artifacts-search.md) | GET | Searches artifacts in Chatvolt AI. |
| [Update Artifact](actions/artifacts-update.md) | PUT | Updates an artifact in Chatvolt AI. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Delete Media](actions/artifacts-media-delete.md) | DELETE | Deletes a media from Chatvolt AI. |
| [List Media](actions/artifacts-media-list.md) | GET | Retrieves media from Chatvolt AI. |
| [Update Media](actions/artifacts-media-update.md) | PUT | Updates a media in Chatvolt AI. |
| [Upload Media](actions/artifacts-media-upload.md) | POST | Uploads media to Chatvolt AI. |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [Unlink Contact from Dispatch](actions/dispatches-contacts-link-delete.md) | DELETE | Unlinks a contact from a dispatch in Chatvolt AI. |
| [Get Contact Links](actions/dispatches-contacts-link-get.md) | GET | Retrieves contact links from Chatvolt AI. |
| [Link Contact to Dispatch](actions/dispatches-contacts-link-post.md) | POST | Links a contact to a dispatch in Chatvolt AI. |
| [Delete a Contact List](actions/dispatches-contacts-lists-delete.md) | DELETE | Deletes a contact list from Chatvolt AI. |
| [Get Contact Lists](actions/dispatches-contacts-lists-get.md) | GET | Retrieves contact lists from Chatvolt AI. |
| [Create or Update a Contact List](actions/dispatches-contacts-lists-post.md) | PUT | Creates a contact list in Chatvolt AI, or updates an existing one. |
| [Edit Contact List](actions/dispatches-contacts-lists-put.md) | PUT | Updates an existing contact list in Chatvolt AI. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Get Messages](actions/conversation-get-messages.md) | GET | Retrieves messages from Chatvolt AI. |
| [Get one Message](actions/conversation-get-one-message.md) | GET | Retrieves a message from Chatvolt AI. |
| [Register Message in Context](actions/conversation-message-register.md) | POST | Registers a message in conversation context in Chatvolt AI. |
| [Send Message by Channel](actions/conversation-send-message.md) | POST | Sends a message by channel through Chatvolt AI. |
| [Send SMS Message](actions/twilio-send-message.md) | POST | Sends an SMS message through Chatvolt AI. |
| [Location Request](actions/whatsapp-location-request.md) | POST | Sends a location request through Chatvolt AI. |
| [Send Buttons](actions/whatsapp-send-buttons.md) | POST | Sends interactive buttons through Chatvolt AI. |
| [Send Contact](actions/whatsapp-send-contact.md) | POST | Sends a contact message through Chatvolt AI. |
| [Send CTA](actions/whatsapp-send-cta.md) | POST | Sends an interactive CTA through Chatvolt AI. |
| [Send List](actions/whatsapp-send-lists.md) | POST | Sends an interactive list through Chatvolt AI. |
| [Send Location](actions/whatsapp-send-location.md) | POST | Sends a location message through Chatvolt AI. |
| [Send WhatsApp Message](actions/zapi-zapi-send-whatsapp-message.md) | POST | Sends a whatsApp Message through Chatvolt AI. |
| [Send a message through the Zapper integration](actions/zapper-send-message.md) | POST | Sends an a message through the Zapper integration through Chatvolt AI. |

### Notes

| Action | Method | Description |
| --- | --- | --- |
| [Create Note](actions/conversation-create-note.md) | POST | Creates a note in Chatvolt AI. |
| [Delete Note](actions/conversation-delete-note.md) | DELETE | Deletes a note from Chatvolt AI. |
| [Get Notes](actions/conversation-get-notes.md) | GET | Retrieves notes from Chatvolt AI. |
| [Update Note](actions/conversation-update-note.md) | PUT | Updates a note in Chatvolt AI. |

### Phone Numbers

| Action | Method | Description |
| --- | --- | --- |
| [Add Number to Whitelist](actions/agents-add-whitelist.md) | POST | Adds a whitelist number in Chatvolt AI. |
| [Delete Agent Blacklist Entry](actions/agents-delete-agent-blacklist-by-id.md) | DELETE | Deletes an agent blacklist entry from Chatvolt AI. |
| [Delete Number from Whitelist](actions/agents-delete-whitelist.md) | DELETE | Deletes a whitelist number from Chatvolt AI. |
| [Get All Blacklist Entries](actions/agents-get-agent-blacklist.md) | GET | Retrieves agent blacklist entries from Chatvolt AI. |
| [Get Agent Blacklist by Agent ID](actions/agents-get-agent-blacklist-by-id.md) | GET | Retrieves agent blacklist entries from Chatvolt AI. |
| [Get Whitelist Numbers](actions/agents-get-whitelist.md) | GET | Retrieves whitelist numbers from Chatvolt AI. |
| [Update Number in Whitelist](actions/agents-patch-whitelist.md) | PUT | Updates a whitelist number in Chatvolt AI. |
| [Add to Agent Blacklist](actions/agents-post-agent-blacklist.md) | POST | Adds an agent blacklist entry in Chatvolt AI. |

### Pipelines

| Action | Method | Description |
| --- | --- | --- |
| [Create CRM Scenario](actions/crm-scenario-create-scenario.md) | POST | Creates a new CRM scenario in Chatvolt AI. |
| [Delete CRM Scenario](actions/crm-scenario-delete-scenario.md) | DELETE | Deletes an existing CRM scenario from Chatvolt AI. |
| [Remove Conversation from CRM Scenario](actions/crm-scenario-delete-scenario-conversation.md) | DELETE | Removes a conversation from a CRM scenario in Chatvolt AI. |
| [List Scenario Conversations](actions/crm-scenario-list-scenario-conversations.md) | GET | Retrieves CRM scenario conversations from Chatvolt AI. |
| [List CRM Scenarios](actions/crm-scenario-list-scenarios.md) | GET | Retrieves CRM scenarios from Chatvolt AI. |
| [Update CRM Scenario](actions/crm-scenario-update-scenario.md) | PUT | Updates an existing CRM scenario in Chatvolt AI. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Get Mercado Livre Products](actions/mercadolivre-get-products.md) | GET | Retrieves Mercado Livre products from Chatvolt AI. |

### Services

| Action | Method | Description |
| --- | --- | --- |
| [Create Agent](actions/agents-create.md) | POST | Creates an agent in Chatvolt AI. |
| [Delete Agent](actions/agents-delete.md) | DELETE | Deletes an agent from Chatvolt AI. |
| [Get Agent](actions/agents-get.md) | GET | Retrieves an agent from Chatvolt AI. |
| [Agent Query](actions/agents-query.md) | POST | Sends a query to an agent in Chatvolt AI. |
| [Update Agent](actions/agents-update.md) | PUT | Updates an agent in Chatvolt AI. |
| [Enable/Disable Agent Integration](actions/agents-webhook.md) | PUT | Enables or disables an agent integration in Chatvolt AI. |

### Stages

| Action | Method | Description |
| --- | --- | --- |
| [Add Conversation to CRM Step](actions/crm-step-add-step-conversation.md) | POST | Adds a conversation to a CRM step in Chatvolt AI. |
| [Create CRM Step](actions/crm-step-create-step.md) | POST | Creates a new CRM step in Chatvolt AI. |
| [Delete CRM Step](actions/crm-step-delete-step.md) | DELETE | Deletes an existing CRM step from Chatvolt AI. |
| [List CRM Steps](actions/crm-step-list-steps.md) | GET | Retrieves CRM steps from Chatvolt AI. |
| [Move Conversation to CRM Step](actions/crm-step-move-step.md) | PUT | Moves a conversation to a CRM step in Chatvolt AI. |
| [Update CRM Step](actions/crm-step-update-step.md) | PUT | Updates an existing CRM step in Chatvolt AI. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Create Meta Template](actions/whatsapp-create-template.md) | POST | Creates a meta Template in Chatvolt AI. |
| [List Meta Templates](actions/whatsapp-list-templates.md) | GET | Retrieves meta Templates from Chatvolt AI. |
| [WhatsApp Template Message](actions/whatsapp-template-message.md) | POST | Sends a WhatsApp template message through Chatvolt AI. |

