# <img src="https://images.mindcloud.co/apps/icons/kommo_1773246605470.png" alt="Kommo logo" width="28" height="28"> Kommo: Universal API

Manage leads, contacts, pipelines, and sales tasks

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/kommo/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 137
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.kommo.com
- **Vendor API docs:** https://developers.kommo.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kommo/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (137)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET |  |

### Bot

| Action | Method | Description |
| --- | --- | --- |
| [List Bots](actions/list-bots.md) | GET |  |
| [Stop Bot](actions/stop-bot.md) | PUT |  |

### Bot Run

| Action | Method | Description |
| --- | --- | --- |
| [Run Bot](actions/run-bot.md) | POST |  |
| [Run Bots](actions/run-bots.md) | POST |  |

### Call

| Action | Method | Description |
| --- | --- | --- |
| [Create Call](actions/create-call.md) | POST |  |

### Catalog

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Update Catalogs](actions/bulk-update-catalogs.md) | PUT |  |
| [Create Catalog](actions/create-catalog.md) | POST |  |
| [Get Catalog](actions/get-catalog.md) | GET |  |
| [List Catalogs](actions/list-catalogs.md) | GET |  |
| [Update Catalog](actions/update-catalog.md) | PUT |  |

### Catalog Custom Field

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Update Catalog Custom Fields](actions/bulk-update-catalog-custom-fields.md) | PUT |  |
| [Create Catalog Custom Field](actions/create-catalog-custom-field.md) | POST |  |
| [Get Catalog Custom Field](actions/get-catalog-custom-field.md) | GET |  |
| [List Catalog Custom Fields](actions/list-catalog-custom-fields.md) | GET |  |
| [Update Catalog Custom Field](actions/update-catalog-custom-field.md) | PUT |  |

### Catalog Element

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Update Catalog Elements](actions/bulk-update-catalog-elements.md) | PUT |  |
| [Create Catalog Element](actions/create-catalog-element.md) | POST |  |
| [Get Catalog Element](actions/get-catalog-element.md) | GET |  |
| [List Catalog Elements](actions/list-catalog-elements.md) | GET |  |
| [Update Catalog Element](actions/update-catalog-element.md) | PUT |  |

### Chat Template

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Update Chat Templates](actions/bulk-update-chat-templates.md) | PUT |  |
| [Create Chat Template](actions/create-chat-template.md) | POST |  |
| [Delete Chat Template](actions/delete-chat-template.md) | DELETE |  |
| [Delete Chat Templates](actions/delete-chat-templates.md) | DELETE |  |
| [Get Chat Template](actions/get-chat-template.md) | GET |  |
| [List Chat Templates](actions/list-chat-templates.md) | GET |  |

### Chat Template Review

| Action | Method | Description |
| --- | --- | --- |
| [Submit Chat Template For Review](actions/submit-chat-template-for-review.md) | PUT |  |
| [Update Chat Template Review](actions/update-chat-template-review.md) | PUT |  |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Update Companies](actions/bulk-update-companies.md) | PUT |  |
| [Create Company](actions/create-company.md) | POST |  |
| [Get Company](actions/get-company.md) | GET |  |
| [List Companies](actions/list-companies.md) | GET |  |
| [Update Company](actions/update-company.md) | PUT |  |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Update Contacts](actions/bulk-update-contacts.md) | PUT |  |
| [Create Contact](actions/create-contact.md) | POST |  |
| [Get Contact](actions/get-contact.md) | GET |  |
| [List Contacts](actions/list-contacts.md) | GET |  |
| [Update Contact](actions/update-contact.md) | PUT |  |

### Contact Chat

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact Chat](actions/create-contact-chat.md) | POST |  |
| [List Contact Chats](actions/list-contact-chats.md) | GET |  |

### Custom Field

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Update Custom Fields](actions/bulk-update-custom-fields.md) | PUT |  |
| [Create Custom Field](actions/create-custom-field.md) | POST |  |
| [Delete Custom Field](actions/delete-custom-field.md) | DELETE |  |
| [Get Custom Field](actions/get-custom-field.md) | GET |  |
| [List Custom Fields](actions/list-custom-fields.md) | GET |  |
| [Update Custom Field](actions/update-custom-field.md) | PUT |  |

### Custom Field Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Field Group](actions/create-custom-field-group.md) | POST |  |
| [Delete Custom Field Group](actions/delete-custom-field-group.md) | DELETE |  |
| [Get Custom Field Group](actions/get-custom-field-group.md) | GET |  |
| [List Custom Field Groups](actions/list-custom-field-groups.md) | GET |  |
| [Update Custom Field Group](actions/update-custom-field-group.md) | PUT |  |

### Entity Link

| Action | Method | Description |
| --- | --- | --- |
| [Link Entity](actions/link-entity.md) | POST |  |
| [List Entity Links](actions/list-entity-links.md) | GET |  |
| [Unlink Entity](actions/unlink-entity.md) | DELETE |  |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Create Event](actions/create-event.md) | POST |  |
| [Get Event](actions/get-event.md) | GET |  |
| [List Events](actions/list-events.md) | GET |  |

### Event Type

| Action | Method | Description |
| --- | --- | --- |
| [List Event Types](actions/list-event-types.md) | GET |  |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Attach Entity File](actions/attach-entity-file.md) | POST |  |
| [Detach Entity File](actions/detach-entity-file.md) | DELETE |  |
| [List Entity Files](actions/list-entity-files.md) | GET |  |

### File Link

| Action | Method | Description |
| --- | --- | --- |
| [List File Links](actions/list-file-links.md) | GET |  |

### Incoming Lead

| Action | Method | Description |
| --- | --- | --- |
| [Accept Incoming Lead](actions/accept-incoming-lead.md) | PUT |  |
| [Create Incoming Call Lead](actions/create-incoming-call-lead.md) | POST |  |
| [Create Incoming Form Lead](actions/create-incoming-form-lead.md) | POST |  |
| [Decline Incoming Lead](actions/decline-incoming-lead.md) | DELETE |  |
| [Get Incoming Lead](actions/get-incoming-lead.md) | GET |  |
| [Link Incoming Lead](actions/link-incoming-lead.md) | PUT |  |
| [List Incoming Leads](actions/list-incoming-leads.md) | GET |  |

### Incoming Lead Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get Incoming Leads Summary](actions/get-incoming-leads-summary.md) | GET |  |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Update Leads](actions/bulk-update-leads.md) | PUT |  |
| [Create Complex Lead](actions/create-complex-lead.md) | POST |  |
| [Create Lead](actions/create-lead.md) | POST |  |
| [Get Lead](actions/get-lead.md) | GET |  |
| [List Leads](actions/list-leads.md) | GET |  |
| [Update Lead](actions/update-lead.md) | PUT |  |

### Loss Reason

| Action | Method | Description |
| --- | --- | --- |
| [Get Loss Reason](actions/get-loss-reason.md) | GET |  |
| [List Loss Reasons](actions/list-loss-reasons.md) | GET |  |

### Note

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Update Notes](actions/bulk-update-notes.md) | PUT |  |
| [Create Note](actions/create-note.md) | POST |  |
| [Get Note](actions/get-note.md) | GET |  |
| [List Notes](actions/list-notes.md) | GET |  |
| [List Notes For Entity](actions/list-notes-for-entity.md) | GET |  |
| [Pin Note](actions/pin-note.md) | PUT |  |
| [Unpin Note](actions/unpin-note.md) | PUT |  |
| [Update Note](actions/update-note.md) | PUT |  |

### Pipeline

| Action | Method | Description |
| --- | --- | --- |
| [Create Pipeline](actions/create-pipeline.md) | POST |  |
| [Delete Pipeline](actions/delete-pipeline.md) | DELETE |  |
| [Get Pipeline](actions/get-pipeline.md) | GET |  |
| [List Pipelines](actions/list-pipelines.md) | GET |  |
| [Update Pipeline](actions/update-pipeline.md) | PUT |  |

### Pipeline Stage

| Action | Method | Description |
| --- | --- | --- |
| [Create Pipeline Stage](actions/create-pipeline-stage.md) | POST |  |
| [Delete Pipeline Stage](actions/delete-pipeline-stage.md) | DELETE |  |
| [Get Pipeline Stage](actions/get-pipeline-stage.md) | GET |  |
| [List Pipeline Stages](actions/list-pipeline-stages.md) | GET |  |
| [Update Pipeline Stage](actions/update-pipeline-stage.md) | PUT |  |

### Role

| Action | Method | Description |
| --- | --- | --- |
| [Create Role](actions/create-role.md) | POST |  |
| [Delete Role](actions/delete-role.md) | DELETE |  |
| [Get Role](actions/get-role.md) | GET |  |
| [List Roles](actions/list-roles.md) | GET |  |
| [Update Role](actions/update-role.md) | PUT |  |

### Salesbot Run

| Action | Method | Description |
| --- | --- | --- |
| [Continue Salesbot](actions/continue-salesbot.md) | PUT |  |
| [Run Salesbot](actions/run-salesbot.md) | POST |  |

### Source

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Update Sources](actions/bulk-update-sources.md) | PUT |  |
| [Create Source](actions/create-source.md) | POST |  |
| [Delete Source](actions/delete-source.md) | DELETE |  |
| [Delete Sources](actions/delete-sources.md) | DELETE |  |
| [Get Source](actions/get-source.md) | GET |  |
| [List Sources](actions/list-sources.md) | GET |  |
| [Update Source](actions/update-source.md) | PUT |  |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Update Entity Tags](actions/bulk-update-entity-tags.md) | PUT |  |
| [Create Tag](actions/create-tag.md) | POST |  |
| [List Tags](actions/list-tags.md) | GET |  |
| [Update Entity Tags](actions/update-entity-tags.md) | PUT |  |

### Talk

| Action | Method | Description |
| --- | --- | --- |
| [Close Talk](actions/close-talk.md) | PUT |  |
| [Get Talk](actions/get-talk.md) | GET |  |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Update Tasks](actions/bulk-update-tasks.md) | PUT |  |
| [Create Task](actions/create-task.md) | POST |  |
| [Get Task](actions/get-task.md) | GET |  |
| [List Tasks](actions/list-tasks.md) | GET |  |
| [Update Task](actions/update-task.md) | PUT |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST |  |
| [Get User](actions/get-user.md) | GET |  |
| [List Users](actions/list-users.md) | GET |  |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST |  |
| [Delete Webhooks](actions/delete-webhooks.md) | DELETE |  |
| [List Webhooks](actions/list-webhooks.md) | GET |  |

### Website Button

| Action | Method | Description |
| --- | --- | --- |
| [Create Website Button](actions/create-website-button.md) | POST |  |
| [Get Website Button](actions/get-website-button.md) | GET |  |
| [List Website Buttons](actions/list-website-buttons.md) | GET |  |
| [Update Website Button](actions/update-website-button.md) | PUT |  |

### Website Button Online Chat

| Action | Method | Description |
| --- | --- | --- |
| [Create Website Button Online Chat](actions/create-website-button-online-chat.md) | POST |  |

### Widget

| Action | Method | Description |
| --- | --- | --- |
| [Delete Widget](actions/delete-widget.md) | DELETE |  |
| [Get Widget](actions/get-widget.md) | GET |  |
| [Install Widget](actions/install-widget.md) | POST |  |
| [List Widgets](actions/list-widgets.md) | GET |  |

