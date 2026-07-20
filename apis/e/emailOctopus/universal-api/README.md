# <img src="https://images.mindcloud.co/apps/icons/email-octopus_1773241658748.png" alt="EmailOctopus logo" width="28" height="28"> EmailOctopus: Universal API

Manage email lists, contacts, and campaigns in EmailOctopus

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/emailOctopus/latest
- **Category:** Communication / Email Communications
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://emailoctopus.com/
- **Vendor API docs:** https://emailoctopus.com/api-documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Lists](actions/list-lists.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emailOctopus/latest/actions/list-lists?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a campaign from EmailOctopus by ID. |
| [Get Campaign Report: Bounced](actions/get-campaign-report-bounced.md) | GET | Retrieves the bounced report for an EmailOctopus campaign. |
| [Get Campaign Report: Clicked](actions/get-campaign-report-clicked.md) | GET | Retrieves the clicked report for an EmailOctopus campaign. |
| [Get Campaign Report: Links](actions/get-campaign-report-links.md) | GET | Retrieves the links report for an EmailOctopus campaign. |
| [Get Campaign Report: Not Clicked](actions/get-campaign-report-not-clicked.md) | GET | Retrieves the not-clicked report for an EmailOctopus campaign. |
| [Get Campaign Report: Opened](actions/get-campaign-report-opened.md) | GET | Retrieves the opened report for an EmailOctopus campaign. |
| [Get Campaign Report: Sent](actions/get-campaign-report-sent.md) | GET | Retrieves the sent report for an EmailOctopus campaign. |
| [Get Campaign Report: Summary](actions/get-campaign-report-summary.md) | GET | Retrieves the summary report for an EmailOctopus campaign. |
| [Get Campaign Report: Unsubscribed](actions/get-campaign-report-unsubscribed.md) | GET | Retrieves the unsubscribed report for an EmailOctopus campaign. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns from EmailOctopus. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a contact in an EmailOctopus list. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes a contact from an EmailOctopus list. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from EmailOctopus by ID. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from an EmailOctopus list. |
| [List Contacts by Tag](actions/list-contacts-by-tag.md) | GET | Retrieves contacts from an EmailOctopus list by tag. |
| [List Subscribed Contacts](actions/list-subscribed-contacts.md) | GET | Retrieves subscribed contacts from an EmailOctopus list. |
| [List Unsubscribed Contacts](actions/list-unsubscribed-contacts.md) | GET | Retrieves unsubscribed contacts from an EmailOctopus list. |
| [Update Contact](actions/update-contact.md) | PUT | Updates a contact in an EmailOctopus list. |
| [Update Multiple Contacts](actions/update-multiple-contacts.md) | PUT | Updates multiple contacts in an EmailOctopus list. |

### List

| Action | Method | Description |
| --- | --- | --- |
| [List Lists](actions/list-lists.md) | GET | Retrieves lists from EmailOctopus. |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [Create List](actions/create-list.md) | POST | Creates a new list in EmailOctopus. |
| [Delete List](actions/delete-list.md) | DELETE | Deletes an existing list from EmailOctopus. |
| [Get List](actions/get-list.md) | GET | Retrieves a list from EmailOctopus by ID. |
| [Update List](actions/update-list.md) | PUT | Updates an existing list in EmailOctopus. |

