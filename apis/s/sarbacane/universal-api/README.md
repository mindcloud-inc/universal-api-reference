# <img src="https://images.mindcloud.co/apps/icons/unnamed-5_1774454362367.png" alt="Sarbacane logo" width="28" height="28"> Sarbacane: Universal API

Sarbacane is an email, SMS, forms, pages, contacts, and campaign platform. This app integrates Sarbacane's REST APIs for account management, contacts, campaigns, pages, and forms.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sarbacane/latest
- **Category:** Marketing
- **Actions:** 32
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.sarbacane.com/en/
- **Vendor API docs:** https://developers.sarbacane.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Credits](actions/get-credits.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sarbacane/latest/actions/get-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (32)

### Audience

| Action | Method | Description |
| --- | --- | --- |
| [Create List](actions/create-list.md) | POST | Creates a new list in Sarbacane. |
| [Delete List](actions/delete-list.md) | DELETE | Deletes an existing list from Sarbacane. |
| [Empty List](actions/empty-list.md) | PUT | Empties an existing list in Sarbacane. |
| [Update List](actions/update-list.md) | PUT | Updates an existing list in Sarbacane. |

### Audiences

| Action | Method | Description |
| --- | --- | --- |
| [List Lists](actions/list-lists.md) | GET | Retrieves lists from your Sarbacane account. |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Add Campaign Blacklists](actions/add-campaign-blacklists.md) | POST | Adds blacklist entries to a campaign in Sarbacane. |
| [Add Campaign Content](actions/add-campaign-content.md) | PUT | Imports template content into a campaign in Sarbacane. |
| [Cancel Campaign](actions/cancel-campaign.md) | PUT | Cancels an existing campaign in Sarbacane. |
| [Create Email Campaign](actions/create-email-campaign.md) | POST | Creates a new email campaign in Sarbacane. |
| [Create SMS Campaign](actions/create-sms-campaign.md) | POST | Creates a new SMS campaign in Sarbacane. |
| [Delete Campaign](actions/delete-campaign.md) | DELETE | Deletes an existing campaign from Sarbacane. |
| [Get Campaign Details](actions/get-campaign-details.md) | GET | Retrieves campaign details from your Sarbacane account. |
| [Import Campaign List](actions/import-campaign-list.md) | POST | Imports a list into a campaign in Sarbacane. |
| [Import Campaign Recipients](actions/import-campaign-recipients.md) | POST | Imports recipients into a campaign in Sarbacane. |
| [Import Campaign Template](actions/import-campaign-template.md) | PUT | Adds content to a campaign send in Sarbacane. |
| [Manage Campaign Teams](actions/manage-campaign-teams.md) | PUT | Updates campaign teams in your Sarbacane account. |
| [Send Campaign](actions/send-campaign.md) | PUT | Sends an existing campaign in Sarbacane. |

### Campaign Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign Statistics](actions/get-campaign-statistics.md) | GET | Retrieves campaign statistics from your Sarbacane account. |

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns from your Sarbacane account. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Add Contact](actions/add-contact.md) | POST | Creates a new contact in Sarbacane. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Sarbacane. |
| [Import Contacts](actions/import-contacts.md) | POST | Imports contacts into a Sarbacane list. |
| [List Campaign Recipients](actions/list-campaign-recipients.md) | GET | Retrieves recipients for a campaign in Sarbacane. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from a Sarbacane list. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Sarbacane. |
| [Upsert Contact](actions/upsert-contact.md) | PUT | Finds a contact in Sarbacane, or creates one if needed. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [List Teams for List](actions/list-teams-for-list.md) | GET | Retrieves groups for a list in Sarbacane. |
| [Update Teams for List](actions/update-teams-for-list.md) | PUT | Updates groups for a list in Sarbacane. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Credits](actions/get-credits.md) | GET | Retrieves account credit details from Sarbacane. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Add Webhook](actions/add-webhook.md) | POST | Creates a new webhook in Sarbacane. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook from your Sarbacane account. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from your Sarbacane account. |

