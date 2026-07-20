# <img src="https://images.mindcloud.co/apps/icons/smoove_1773772468976.png" alt="Smoove logo" width="28" height="28"> Smoove: Universal API

Manage contacts, lists, campaigns, and landing page leads

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/smoove/latest
- **Category:** Marketing
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.smoove.io
- **Vendor API docs:** https://rest.smoove.io

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Active Contacts](actions/list-active-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smoove/latest/actions/list-active-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Create Campaign](actions/create-campaign.md) | POST | Creates a new email campaign in Smoove. |
| [Delete Campaign](actions/delete-campaign.md) | DELETE | Deletes an existing email campaign from Smoove. |
| [Get Campaign Statistics](actions/get-campaign-statistics.md) | GET | Retrieves aggregated statistics for a Smoove email campaign. |
| [Send Campaign](actions/send-campaign.md) | PUT | Sends a saved email campaign in Smoove. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Check Contact Exists](actions/check-contact-exists.md) | GET | Checks whether a contact exists in Smoove. |
| [Create Or Update Contact](actions/create-or-update-contact.md) | POST | Creates a new contact in Smoove, or updates an existing one. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Smoove by identifier. |
| [Import Contacts in Bulk](actions/import-contacts-in-bulk.md) | POST | Imports contacts into Smoove in bulk. |
| [List Active Contacts](actions/list-active-contacts.md) | GET | Retrieves active contacts from Smoove. |
| [List Blacklisted Contacts](actions/list-blacklisted-contacts.md) | GET | Retrieves blacklisted contacts from Smoove. |
| [List Unsubscribed Contacts](actions/list-unsubscribed-contacts.md) | GET | Retrieves unsubscribed contacts from Smoove. |
| [Resubscribe Contact](actions/resubscribe-contact.md) | PUT | Resubscribes a contact to Smoove campaigns and lists. |
| [Unsubscribe Contact](actions/unsubscribe-contact.md) | PUT | Unsubscribes a contact from Smoove campaigns and lists. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Smoove by identifier. |

### Contact Field

| Action | Method | Description |
| --- | --- | --- |
| [List Contact Fields](actions/list-contact-fields.md) | GET | Retrieves contact field definitions from Smoove. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [List Campaign Recipients](actions/list-campaign-recipients.md) | GET | Retrieves recipient responses for a Smoove email campaign. |
| [List Contacts In List](actions/list-contacts-in-list.md) | GET | Retrieves contacts from a specific Smoove list. |
| [List Landing Page Recipients](actions/list-landing-page-recipients.md) | GET | Retrieves subscribers for a Smoove landing page. |

### Landing Pages

| Action | Method | Description |
| --- | --- | --- |
| [Get Landing Page](actions/get-landing-page.md) | GET | Retrieves a landing page from Smoove. |
| [List Landing Pages](actions/list-landing-pages.md) | GET | Retrieves landing pages from Smoove. |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [Create List](actions/create-list.md) | POST | Creates a new contact list in Smoove. |
| [Get List](actions/get-list.md) | GET | Retrieves a contact list from Smoove. |
| [List Contact Lists](actions/list-contact-lists.md) | GET | Retrieves contact lists from Smoove. |

