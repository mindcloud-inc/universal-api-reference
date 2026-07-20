# <img src="https://images.mindcloud.co/apps/icons/active-campaign-logo_1772729882616.png" alt="ActiveCampaign logo" width="28" height="28"> ActiveCampaign: Universal API

Manage contacts, automate campaigns, track deals, and grow customer relationships.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/activeCampaign/latest
- **Category:** Marketing
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.activecampaign.com
- **Vendor API docs:** https://developers.activecampaign.com/reference/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contacts](actions/list-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activeCampaign/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Create Account](actions/create-account.md) | POST | Creates a new account in ActiveCampaign. |
| [Get Account](actions/get-account.md) | GET | Retrieves an account from ActiveCampaign. |
| [List Accounts](actions/list-accounts.md) | GET | Retrieves accounts from ActiveCampaign. |
| [Update Account](actions/update-account.md) | PUT | Updates an existing account in ActiveCampaign. |

### Automation

| Action | Method | Description |
| --- | --- | --- |
| [List Automations](actions/list-automations.md) | GET | Retrieves automations from ActiveCampaign. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in ActiveCampaign. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from ActiveCampaign. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from ActiveCampaign. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from ActiveCampaign. |
| [Sync Contact](actions/sync-contact.md) | POST | Finds a contact in ActiveCampaign, or creates one if no match is found. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in ActiveCampaign. |

### Contact Automation

| Action | Method | Description |
| --- | --- | --- |
| [Add Contact To Automation](actions/add-contact-to-automation.md) | POST | Adds a contact to an automation in ActiveCampaign. |
| [List Contact Automations](actions/list-contact-automations.md) | GET | Retrieves contact automations from ActiveCampaign. |
| [Remove Contact From Automation](actions/remove-contact-from-automation.md) | DELETE | Removes a contact from an automation in ActiveCampaign. |

### Contact List

| Action | Method | Description |
| --- | --- | --- |
| [Update Contact List Status](actions/update-contact-list-status.md) | PUT | Updates a contact's list status in ActiveCampaign. |

### Contact Tag

| Action | Method | Description |
| --- | --- | --- |
| [Add Tag To Contact](actions/add-tag-to-contact.md) | POST | Adds a tag to a contact in ActiveCampaign. |
| [Remove Tag From Contact](actions/remove-tag-from-contact.md) | DELETE | Removes a tag from a contact in ActiveCampaign. |

### Deal

| Action | Method | Description |
| --- | --- | --- |
| [Create Deal](actions/create-deal.md) | POST | Creates a new deal in ActiveCampaign. |
| [Delete Deal](actions/delete-deal.md) | DELETE | Deletes an existing deal from ActiveCampaign. |
| [Get Deal](actions/get-deal.md) | GET | Retrieves a deal from ActiveCampaign. |
| [List Deals](actions/list-deals.md) | GET | Retrieves deals from ActiveCampaign. |
| [Update Deal](actions/update-deal.md) | PUT | Updates an existing deal in ActiveCampaign. |

### Deal Stage

| Action | Method | Description |
| --- | --- | --- |
| [List Deal Stages](actions/list-deal-stages.md) | GET | Retrieves deal stages from ActiveCampaign. |

### Field Value

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Field Value](actions/create-custom-field-value.md) | POST | Creates a custom field value in ActiveCampaign. |
| [List Custom Field Values](actions/list-custom-field-values.md) | GET | Retrieves custom field values from ActiveCampaign. |
| [Update Custom Field Value For Contact](actions/update-custom-field-value-for-contact.md) | PUT | Updates a contact custom field value in ActiveCampaign. |

### List

| Action | Method | Description |
| --- | --- | --- |
| [Create List](actions/create-list.md) | POST | Creates a new list in ActiveCampaign. |
| [Delete List](actions/delete-list.md) | DELETE | Deletes an existing list from ActiveCampaign. |
| [Get List](actions/get-list.md) | GET | Retrieves a list from ActiveCampaign. |
| [List Lists](actions/list-lists.md) | GET | Retrieves lists from ActiveCampaign. |

### Pipeline

| Action | Method | Description |
| --- | --- | --- |
| [List Pipelines](actions/list-pipelines.md) | GET | Retrieves pipelines from ActiveCampaign. |

