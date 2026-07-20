# <img src="https://images.mindcloud.co/apps/icons/spoki_1773782693060.png" alt="Spoki logo" width="28" height="28"> Spoki: Universal API

Spoki: Manage WhatsApp contacts, campaigns, automations, and templates

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/spoki/latest
- **Category:** Communication / Team Messaging
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://app.spoki.com/
- **Vendor API docs:** https://documenter.getpostman.com/view/21611004/UzBqnPvF

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Templates](actions/list-templates.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoki/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Automation

| Action | Method | Description |
| --- | --- | --- |
| [Create Automation](actions/create-automation.md) | POST | Creates an automation with steps, triggers, and optional automation groups. |
| [List Automations](actions/list-automations.md) | GET | Lists and searches automations for the authenticated account. |
| [Retrieve Automation](actions/retrieve-automation.md) | GET | Retrieves an automation by ID. |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Create Campaign](actions/create-campaign.md) | POST | Creates a campaign from an existing automation or template. |
| [List Campaigns](actions/list-campaigns.md) | GET | Lists campaigns for the authenticated account, including status and delivery metrics. |
| [Retrieve Campaign](actions/retrieve-campaign.md) | GET | Retrieves a campaign by ID. |
| [Update Campaign](actions/update-campaign.md) | PUT | Updates a campaign by ID, including scheduling, status, or list settings. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes a contact by ID. |
| [List Contacts](actions/list-contacts.md) | GET | Lists and searches contacts for the authenticated account. |
| [Retrieve Contact](actions/retrieve-contact.md) | GET | Retrieves a contact by ID. |
| [Sync Contacts](actions/sync-contacts.md) | POST | Creates a contact or updates an existing one using the provided contact data. |
| [Update Contact](actions/update-contact.md) | PUT | Updates a contact by ID. |

### List

| Action | Method | Description |
| --- | --- | --- |
| [Create List](actions/create-list.md) | POST | Creates a new contact list. |
| [List Lists](actions/list-lists.md) | GET | Lists and searches contact lists for the authenticated account. |
| [Retrieve List](actions/retrieve-list.md) | GET | Retrieves a contact list by ID. |
| [Sync List Contacts](actions/sync-list-contacts.md) | PUT | Creates or updates up to 500 contacts and adds them to the selected list. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | POST | Creates a WhatsApp template for the authenticated account or a specific active WhatsApp channel. |
| [List Templates](actions/list-templates.md) | GET | Lists templates for the authenticated account, with optional filtering by channel-specific WABA. |
| [Retrieve Template](actions/retrieve-template.md) | GET | Retrieves a template by ID, with optional channel scoping for multi-WABA accounts. |
| [Update Template](actions/update-template.md) | PUT | Updates an existing WhatsApp template by ID with partial changes. |

