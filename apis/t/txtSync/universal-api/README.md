# <img src="https://images.mindcloud.co/apps/icons/txt-sync_1774295767637.png" alt="TxtSync logo" width="28" height="28"> TxtSync: Universal API

Send SMS, manage contacts, and run text campaigns

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/txtSync/latest
- **Category:** Marketing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://txtsync.com/
- **Vendor API docs:** https://docs.txtsync.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get System Report](actions/get-system-report.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/txtSync/latest/actions/get-system-report?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Activate Campaign](actions/activate-campaign.md) | PUT | Activates an existing campaign in TxtSync. |
| [Add Campaign Connection](actions/add-campaign-connection.md) | POST | Adds recipients to a campaign in TxtSync. |
| [Create Campaign](actions/create-campaign.md) | POST | Creates a new campaign in TxtSync. |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a specific campaign from TxtSync. |
| [Get Campaign Report](actions/get-campaign-report.md) | GET | Retrieves a campaign report from TxtSync. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns from TxtSync. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Check Contact Duplicates](actions/check-contact-duplicates.md) | GET | Retrieves duplicate contact matches from TxtSync. |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in TxtSync. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from TxtSync. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a specific contact from TxtSync. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from TxtSync. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in TxtSync. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [List SMS](actions/list-sms.md) | GET | Retrieves SMS messages from TxtSync. |
| [Preview SMS](actions/preview-sms.md) | GET | Previews an SMS message in TxtSync. |
| [Send Bulk SMS](actions/send-bulk-sms.md) | POST | Creates bulk SMS messages in TxtSync. |
| [Send Single SMS](actions/send-single-sms.md) | POST | Creates a single SMS message in TxtSync. |

### System Report

| Action | Method | Description |
| --- | --- | --- |
| [Get System Report](actions/get-system-report.md) | GET | Retrieves the system report from TxtSync. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Add Contact Tags](actions/add-contact-tags.md) | POST | Adds tags to a contact in TxtSync. |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag in TxtSync. |
| [Delete Tag](actions/delete-tag.md) | DELETE | Deletes an existing tag from TxtSync. |
| [Get Tag](actions/get-tag.md) | GET | Retrieves a specific tag from TxtSync. |
| [List Contact Tags](actions/list-contact-tags.md) | GET | Retrieves tags associated with a contact in TxtSync. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from TxtSync. |
| [Update Tag](actions/update-tag.md) | PUT | Updates an existing tag in TxtSync. |

