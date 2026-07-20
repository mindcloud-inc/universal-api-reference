# <img src="https://images.mindcloud.co/apps/icons/direct-iq_1782742806404.png" alt="DirectIQ logo" width="28" height="28"> DirectIQ: Universal API

Manage contacts, lists, campaigns, and templates in DirectIQ

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/directiq/latest
- **Category:** Marketing
- **Actions:** 95
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.directiq.com
- **Vendor API docs:** https://directiq.readme.io/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contacts](actions/list-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/directiq/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (95)

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Create Campaign Overview Export](actions/create-campaign-overview-export.md) | POST | Creates a campaign overview export in DirectIQ. |
| [Create regular campaign](actions/create-regular-campaign.md) | POST | Creates a regular campaign in DirectIQ. |
| [Create Statistics Export](actions/create-statistics-export.md) | POST | Creates a campaign statistics export in DirectIQ. |
| [Get bounce report](actions/get-bounce-report.md) | GET | Retrieves campaign bounce records from DirectIQ. |
| [Get campaign](actions/get-campaign.md) | GET | Retrieves a campaign from DirectIQ by ID. |
| [Get click report](actions/get-click-report.md) | GET | Retrieves campaign click records from DirectIQ. |
| [Get complaint report](actions/get-complaint-report.md) | GET | Retrieves campaign complaint records from DirectIQ. |
| [Get Document](actions/get-document.md) | GET | Downloads a document from DirectIQ by ID. |
| [Get domain report](actions/get-domain-report.md) | GET | Retrieves campaign domain details from DirectIQ. |
| [Get email client report](actions/get-email-client-report.md) | GET | Retrieves campaign email client details from DirectIQ. |
| [Get open report](actions/get-open-report.md) | GET | Retrieves campaign open records from DirectIQ. |
| [Get opens from social media campaign](actions/get-opens-from-social-media-campaign.md) | GET | Retrieves social media campaign opens from DirectIQ. |
| [Get pricing](actions/get-pricing.md) | GET | Retrieves current pricing details from DirectIQ. |
| [Get recipient report](actions/get-recipient-report.md) | GET | Retrieves campaign recipient records from DirectIQ. |
| [Get unsubscribe report](actions/get-unsubscribe-report.md) | GET | Retrieves campaign unsubscribe records from DirectIQ. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves a paginated list of campaigns from DirectIQ. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Add a note to contact](actions/add-a-note-to-contact.md) | PUT | Adds a note to a contact in DirectIQ. |
| [Create contact key](actions/create-contact-key.md) | POST | Creates a contact key in DirectIQ. |
| [Create Contacts Export](actions/create-contacts-export.md) | POST | Creates a contacts export in DirectIQ. |
| [Create subscription](actions/create-subscription.md) | POST | Creates a contact subscription in DirectIQ. |
| [Delete a contact](actions/delete-a-contact.md) | DELETE | Deletes an existing contact from DirectIQ. |
| [Delete a contact key](actions/delete-a-contact-key.md) | DELETE | Deletes a contact key from DirectIQ. |
| [Delete Contacts in Bulk](actions/delete-contacts-in-bulk.md) | DELETE | Deletes multiple existing contacts from DirectIQ. |
| [Get a contact](actions/get-a-contact.md) | GET | Retrieves a contact from DirectIQ by ID. |
| [Get a contact activity](actions/get-a-contact-activity.md) | GET | Retrieves a contact activity from DirectIQ by ID. |
| [Get contact details](actions/get-contact-details.md) | GET | Retrieves detailed contact information from DirectIQ. |
| [Get number of contacts](actions/get-number-of-contacts.md) | GET | Retrieves the total number of contacts in DirectIQ. |
| [Get subscription authorization settings](actions/get-subscription-authorization-settings.md) | GET | Retrieves subscription authorization settings from DirectIQ. |
| [List Active and Disabled Contacts](actions/list-active-and-disabled-contacts.md) | GET | Retrieves active and disabled contact counts from DirectIQ. |
| [List Client Contact Keys](actions/list-client-contact-keys.md) | GET | Retrieves client contact keys from DirectIQ. |
| [List Contact Keys](actions/list-contact-keys.md) | GET | Retrieves contact keys from DirectIQ. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves a paginated list of contacts from DirectIQ. |
| [List Custom Fields](actions/list-custom-fields.md) | GET | Retrieves custom fields from DirectIQ. |
| [List Date Formats](actions/list-date-formats.md) | GET | Retrieves available date formats from DirectIQ. |
| [List Date Keys](actions/list-date-keys.md) | GET | Retrieves date-type contact keys from DirectIQ. |
| [List Passive Contacts](actions/list-passive-contacts.md) | GET | Retrieves a paginated list of passive contacts from DirectIQ. |
| [Remove a note from contact](actions/remove-a-note-from-contact.md) | DELETE | Deletes a note from a contact in DirectIQ. |
| [Search Contacts](actions/search-contacts.md) | GET | Finds contacts in DirectIQ created after a given date. |
| [Set Contact Active](actions/set-contact-active.md) | PUT | Sets a contact to active in DirectIQ. |
| [Set Contact Disabled](actions/set-contact-disabled.md) | PUT | Sets a contact to manually disabled in DirectIQ. |
| [Set Contacts Active in Bulk](actions/set-contacts-active-in-bulk.md) | PUT | Sets multiple contacts to active in DirectIQ. |
| [Set Contacts Disabled in Bulk](actions/set-contacts-disabled-in-bulk.md) | PUT | Sets multiple contacts to manually disabled in DirectIQ. |
| [Update a contact](actions/update-a-contact.md) | PUT | Updates an existing contact in DirectIQ. |
| [Update a contact note](actions/update-a-contact-note.md) | PUT | Updates a note on a contact in DirectIQ. |
| [Update Contact Details](actions/update-contact-details.md) | PUT | Updates detailed contact information in DirectIQ. |
| [Update contact key](actions/update-contact-key.md) | PUT | Updates an existing contact key in DirectIQ. |
| [Update contact key visibility](actions/update-contact-key-visibility.md) | PUT | Updates contact key visibility in DirectIQ. |
| [Update contact keys](actions/update-contact-keys.md) | PUT | Updates contact key display order and visibility in DirectIQ. |
| [Update Subscription Authorization Settings](actions/update-subscription-authorization-settings.md) | GET | Updates subscription authorization settings in DirectIQ. |

### Emails

| Action | Method | Description |
| --- | --- | --- |
| [Add Tag to Template](actions/add-tag-to-template.md) | PUT | Adds a tag to a template in DirectIQ. |
| [Create a template](actions/create-a-template.md) | POST | Creates a template in DirectIQ. |
| [Get a template](actions/get-a-template.md) | GET | Retrieves a template from DirectIQ by ID. |
| [Get template HTML](actions/get-template-html.md) | GET | Retrieves a template's HTML content from DirectIQ. |
| [List Templates](actions/list-templates.md) | GET | Retrieves all templates from DirectIQ. |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [Add a contact to a list](actions/add-a-contact-to-a-list.md) | PUT | Adds a contact to a list in DirectIQ. |
| [Add a tag to contacts](actions/add-a-tag-to-contacts.md) | PUT | Adds a tag to multiple contacts in DirectIQ. |
| [Add Contacts to List](actions/add-contacts-to-list.md) | PUT | Adds multiple contacts to a list in DirectIQ. |
| [Add or Create Tag for Contact](actions/add-or-create-tag-for-contact.md) | POST | Adds a tag to a contact or creates one in DirectIQ. |
| [Add Tag to Contact](actions/add-tag-to-contact.md) | PUT | Adds a tag to a contact in DirectIQ. |
| [Create a client tag](actions/create-a-client-tag.md) | POST | Creates a client tag in DirectIQ. |
| [Create a contact list](actions/create-a-contact-list.md) | POST | Creates a contact list in DirectIQ. |
| [Create a segment](actions/create-a-segment.md) | POST | Creates a segment in DirectIQ. |
| [Create a tag](actions/create-a-tag.md) | POST | Creates a tag in DirectIQ. |
| [Create Combined Contact List](actions/create-combined-contact-list.md) | PUT | Combines multiple contact lists into one in DirectIQ. |
| [Create Segment Copy](actions/create-segment-copy.md) | POST | Creates a copy of a segment in DirectIQ. |
| [Delete a contact list](actions/delete-a-contact-list.md) | DELETE | Deletes a contact list from DirectIQ and contacts only on it. |
| [Delete a segment](actions/delete-a-segment.md) | DELETE | Deletes a segment from DirectIQ. |
| [Delete a suppression list](actions/delete-a-suppression-list.md) | DELETE | Deletes a suppression list from DirectIQ. |
| [Delete a tag](actions/delete-a-tag.md) | DELETE | Deletes a tag from DirectIQ. |
| [Delete Contact Lists in Bulk](actions/delete-contact-lists-in-bulk.md) | DELETE | Deletes multiple contact lists from DirectIQ. |
| [Delete contacts from a list](actions/delete-contacts-from-a-list.md) | DELETE | Deletes contacts from a specific list in DirectIQ. |
| [Delete contacts from suppression list](actions/delete-contacts-from-suppression-list.md) | DELETE | Deletes contacts from a suppression list in DirectIQ. |
| [Delete Unused Lists in Bulk](actions/delete-unused-lists-in-bulk.md) | DELETE | Deletes unused contact lists from DirectIQ. |
| [Get a contact list](actions/get-a-contact-list.md) | GET | Retrieves a contact list from DirectIQ by ID. |
| [Get a segment](actions/get-a-segment.md) | GET | Retrieves a segment from DirectIQ by ID. |
| [Get a suppression list](actions/get-a-suppression-list.md) | GET | Retrieves a suppression list from DirectIQ by ID. |
| [Get a tag](actions/get-a-tag.md) | GET | Retrieves a tag from DirectIQ by ID. |
| [Get Tag Validation](actions/get-tag-validation.md) | GET | Checks whether tags are valid in DirectIQ. |
| [List Contact Lists](actions/list-contact-lists.md) | GET | Retrieves all contact lists from DirectIQ. |
| [List Segment Contacts](actions/list-segment-contacts.md) | GET | Retrieves contacts matching segment criteria in DirectIQ. |
| [List Segments](actions/list-segments.md) | GET | Retrieves all segments from DirectIQ. |
| [List Segments for a Contact](actions/list-segments-for-a-contact.md) | GET | Retrieves segments for a contact in DirectIQ. |
| [List Subscription Lists](actions/list-subscription-lists.md) | GET | Retrieves subscription lists from DirectIQ. |
| [List Suppression Lists](actions/list-suppression-lists.md) | GET | Retrieves all suppression lists from DirectIQ. |
| [List Tags](actions/list-tags.md) | GET | Retrieves all tags from DirectIQ. |
| [Remove a contact by email from a list](actions/remove-a-contact-by-email-from-a-list.md) | PUT | Removes a contact from a DirectIQ list by email. |
| [Remove a contact from a list](actions/remove-a-contact-from-a-list.md) | PUT | Removes a contact from a list in DirectIQ. |
| [Remove a tag from a contact using tag name and contact email](actions/remove-a-tag-from-a-contact-using-tag-name-and-contact-email.md) | PUT | Removes a tag from a DirectIQ contact by tag name and email. |
| [Remove a tag from contacts](actions/remove-a-tag-from-contacts.md) | PUT | Removes a tag from multiple contacts in DirectIQ. |
| [Remove Inactive Contacts from Lists](actions/remove-inactive-contacts-from-lists.md) | PUT | Removes inactive contacts from specified DirectIQ lists. |
| [Rename a segment](actions/rename-a-segment.md) | PUT | Renames a segment in DirectIQ. |
| [Rename a suppression list](actions/rename-a-suppression-list.md) | PUT | Renames a suppression list in DirectIQ. |
| [Update a contact list](actions/update-a-contact-list.md) | PUT | Updates an existing contact list in DirectIQ. |
| [Update a segment](actions/update-a-segment.md) | PUT | Updates an existing segment in DirectIQ. |
| [Update a tag](actions/update-a-tag.md) | PUT | Updates an existing tag in DirectIQ. |

