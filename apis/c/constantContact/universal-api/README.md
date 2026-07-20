# <img src="https://images.mindcloud.co/apps/icons/constant-contact_1772638562291.png" alt="Constant Contact logo" width="28" height="28"> Constant Contact: Universal API

Create campaigns, grow contact lists, automate messages, and track marketing results.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/constantContact/latest
- **Category:** Marketing
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.constantcontact.com
- **Vendor API docs:** https://developer.constantcontact.com/api_guide/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Contact Consent Counts](actions/get-contact-consent-counts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/get-contact-consent-counts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a contact in Constant Contact. |
| [Create or Update Contact](actions/create-or-update-contact.md) | POST | Creates or updates a contact in Constant Contact. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes a contact from Constant Contact. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Constant Contact. |
| [Get Contact Consent Counts](actions/get-contact-consent-counts.md) | GET | Retrieves contact consent counts from Constant Contact. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contact records from Constant Contact. |
| [Resubscribe Contact](actions/resubscribe-contact.md) | PUT | Resubscribes a contact in Constant Contact. |
| [Update Contact](actions/update-contact.md) | PUT | Updates a contact in Constant Contact. |

### Contact List

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact List](actions/create-contact-list.md) | POST | Creates a contact list in Constant Contact. |
| [Delete Contact List](actions/delete-contact-list.md) | DELETE | Deletes a contact list from Constant Contact. |
| [Get Contact List](actions/get-contact-list.md) | GET | Retrieves a contact list from Constant Contact. |
| [List Contact Lists](actions/list-contact-lists.md) | GET | Retrieves contact lists from Constant Contact. |
| [Update Contact List](actions/update-contact-list.md) | PUT | Updates a contact list in Constant Contact. |

### Contact Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact Tag](actions/create-contact-tag.md) | POST | Creates a contact tag in Constant Contact. |
| [Delete Contact Tag](actions/delete-contact-tag.md) | DELETE | Deletes a contact tag from Constant Contact. |
| [Get Contact Tag](actions/get-contact-tag.md) | GET | Retrieves a contact tag from Constant Contact. |
| [List Contact Tags](actions/list-contact-tags.md) | GET | Retrieves contact tags from Constant Contact. |
| [Update Contact Tag](actions/update-contact-tag.md) | PUT | Renames a contact tag in Constant Contact. |

### Custom Field

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact Custom Field](actions/create-contact-custom-field.md) | POST | Creates a contact custom field in Constant Contact. |
| [Delete Contact Custom Field](actions/delete-contact-custom-field.md) | DELETE | Deletes a contact custom field from Constant Contact. |
| [List Contact Custom Fields](actions/list-contact-custom-fields.md) | GET | Retrieves contact custom fields from Constant Contact. |
| [Update Contact Custom Field](actions/update-contact-custom-field.md) | PUT | Updates a contact custom field in Constant Contact. |

### Email Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Create Email Campaign](actions/create-email-campaign.md) | POST | Creates an email campaign in Constant Contact. |
| [Delete Email Campaign](actions/delete-email-campaign.md) | DELETE | Deletes an email campaign from Constant Contact. |
| [Get Email Campaign](actions/get-email-campaign.md) | GET | Retrieves an email campaign from Constant Contact. |
| [List Email Campaigns](actions/list-email-campaigns.md) | GET | Retrieves email campaigns from Constant Contact. |
| [Rename Email Campaign](actions/rename-email-campaign.md) | PUT | Renames an email campaign in Constant Contact. |

### Email Campaign Activity

| Action | Method | Description |
| --- | --- | --- |
| [Get Email Campaign Activity](actions/get-email-campaign-activity.md) | GET | Retrieves an email campaign activity from Constant Contact. |

### Email Campaign Schedule

| Action | Method | Description |
| --- | --- | --- |
| [Schedule Email Campaign Activity](actions/schedule-email-campaign-activity.md) | POST | Schedules an email campaign activity in Constant Contact. |

### Email Campaign Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get Email Campaign Summary Report](actions/get-email-campaign-summary-report.md) | GET | Retrieves an email campaign summary report from Constant Contact. |

