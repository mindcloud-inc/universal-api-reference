# <img src="https://images.mindcloud.co/apps/icons/193ef207-80a1-4661-857c-1f5457662d48-0_1776093507257.png" alt="NobelSMS logo" width="28" height="28"> NobelSMS: Universal API

Send campaigns, automate notifications, and manage SMS delivery with NobelSMS

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nobelSMS/latest
- **Category:** Communication / Team Messaging
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://nobelsms.com
- **Vendor API docs:** https://api.nobelsms.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Balances](actions/list-balances.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nobelSMS/latest/actions/list-balances?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Balance](actions/get-balance.md) | GET | Retrieves a balance from NobelSMS by ID. |
| [List Balances](actions/list-balances.md) | GET | Retrieves balances from NobelSMS. |

### Blacklistentry

| Action | Method | Description |
| --- | --- | --- |
| [Create Blacklist Entry](actions/create-blacklist-entry.md) | POST | Creates a new blacklist entry in NobelSMS. |
| [Delete Blacklist Entry](actions/delete-blacklist-entry.md) | DELETE | Deletes a blacklist entry from NobelSMS. |
| [List Blacklist Entries](actions/list-blacklist-entries.md) | GET | Retrieves blacklist entries from NobelSMS. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in NobelSMS. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from NobelSMS. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from NobelSMS by ID. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from NobelSMS. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in NobelSMS. |

### Smstemplate

| Action | Method | Description |
| --- | --- | --- |
| [Create SMS Template](actions/create-sms-template.md) | POST | Creates a new SMS template in NobelSMS. |
| [Delete SMS Template](actions/delete-sms-template.md) | DELETE | Deletes an existing SMS template from NobelSMS. |
| [Get SMS Template](actions/get-sms-template.md) | GET | Retrieves an SMS template from NobelSMS by ID. |
| [List SMS Templates](actions/list-sms-templates.md) | GET | Retrieves SMS templates from NobelSMS. |
| [Update SMS Template](actions/update-sms-template.md) | PUT | Updates an existing SMS template in NobelSMS. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag in NobelSMS. |
| [Delete Tag](actions/delete-tag.md) | DELETE | Deletes an existing tag from NobelSMS. |
| [Get Tag](actions/get-tag.md) | GET | Retrieves a tag from NobelSMS by ID. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from NobelSMS. |
| [Update Tag](actions/update-tag.md) | PUT | Updates an existing tag in NobelSMS. |

