# DirectIQ: Native API Reference

A consolidated summary of DirectIQ's API configuration and 95 documented operations, with links to official documentation.

- **Official docs:** https://directiq.readme.io/reference
- **API base URL:** `https://rest.directiq.com`

## Authentication

### Basic

Basic authentication using your DirectIQ account credentials.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://directiq.readme.io/reference/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `result`. The current page number is read from `pageNumber`.

## Pagination

Use `pageSize` in the query string to set the page size (default 50; accepted range 50–500). Use `pageNumber` in the query string to choose the page; numbering starts at 1.

## Endpoints (95 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add a contact to a list](actions/add-a-contact-to-a-list.md) | `PUT /contacts/lists/addcontact/{id}` | [docs](https://directiq.readme.io/reference/put_lists-addcontact-id) |
| [Add a note to contact](actions/add-a-note-to-contact.md) | `POST /contacts/contactnotes/addnote/{id}` | [docs](https://directiq.readme.io/reference/post_contactnotes-addnote-id) |
| [Add a tag to contacts](actions/add-a-tag-to-contacts.md) | `PUT /contacts/tag/addcontacts/{id}` | [docs](https://directiq.readme.io/reference/put_tag-addcontacts-id) |
| [Add Contacts to List](actions/add-contacts-to-list.md) | `POST /contacts/lists/importcontacts/{id}` | [docs](https://directiq.readme.io/reference/post_lists-importcontacts-id) |
| [Add or Create Tag for Contact](actions/add-or-create-tag-for-contact.md) | `POST /contacts/tag/createorassign` | [docs](https://directiq.readme.io/reference/post_tag-createorassign) |
| [Add Tag to Contact](actions/add-tag-to-contact.md) | `POST /contacts/tag/assign` | [docs](https://directiq.readme.io/reference/post_tag-assign) |
| [Add Tag to Template](actions/add-tag-to-template.md) | `POST /core/template/assigntag/{id}` | [docs](https://directiq.readme.io/reference/post_template-assigntag-id) |
| [Create a client tag](actions/create-a-client-tag.md) | `POST /core/client/createtag` | [docs](https://directiq.readme.io/reference/post_client-createtag) |
| [Create a contact list](actions/create-a-contact-list.md) | `POST /contacts/lists/create` | [docs](https://directiq.readme.io/reference/post_lists-create) |
| [Create a segment](actions/create-a-segment.md) | `POST /contacts/segment/create` | [docs](https://directiq.readme.io/reference/post_segment-create) |
| [Create a tag](actions/create-a-tag.md) | `POST /contacts/tag/create` | [docs](https://directiq.readme.io/reference/post_tag-create) |
| [Create a template](actions/create-a-template.md) | `POST /core/template/create` | [docs](https://directiq.readme.io/reference/post_template-create) |
| [Create Campaign Overview Export](actions/create-campaign-overview-export.md) | `POST /core/export/campaignoverview` | [docs](https://directiq.readme.io/reference/post_export-campaignoverview) |
| [Create Combined Contact List](actions/create-combined-contact-list.md) | `POST /contacts/lists/combinelists` | [docs](https://directiq.readme.io/reference/post_lists-combinelists) |
| [Create contact key](actions/create-contact-key.md) | `POST /contacts/extradata/create` | [docs](https://directiq.readme.io/reference/post_extradata-create) |
| [Create Contacts Export](actions/create-contacts-export.md) | `POST /core/export/contacts` | [docs](https://directiq.readme.io/reference/post_export-contacts) |
| [Create regular campaign](actions/create-regular-campaign.md) | `POST /core/campaign/create` | [docs](https://directiq.readme.io/reference/post_campaign-create) |
| [Create Segment Copy](actions/create-segment-copy.md) | `POST /contacts/segment/duplicate` | [docs](https://directiq.readme.io/reference/post_segment-duplicate) |
| [Create Statistics Export](actions/create-statistics-export.md) | `POST /core/export/statistics` | [docs](https://directiq.readme.io/reference/post_export-statistics) |
| [Create subscription](actions/create-subscription.md) | `POST /subscription/subscribe` | [docs](https://directiq.readme.io/reference/post_subscribe) |
| [Delete a contact](actions/delete-a-contact.md) | `DELETE /contacts/contact/delete/{id}` | [docs](https://directiq.readme.io/reference/delete_contact-delete-id) |
| [Delete a contact key](actions/delete-a-contact-key.md) | `DELETE /contacts/extradata/delete/{id}` | [docs](https://directiq.readme.io/reference/delete_extradata-delete-id) |
| [Delete a contact list](actions/delete-a-contact-list.md) | `DELETE /contacts/lists/delete/{id}` | [docs](https://directiq.readme.io/reference/delete_lists-delete-id) |
| [Delete a segment](actions/delete-a-segment.md) | `DELETE /contacts/segment/delete/{id}` | [docs](https://directiq.readme.io/reference/delete_segment-delete-id) |
| [Delete a suppression list](actions/delete-a-suppression-list.md) | `DELETE /contacts/suppressionlist/delete/{id}` | [docs](https://directiq.readme.io/reference/delete_suppressionlist-delete-id) |
| [Delete a tag](actions/delete-a-tag.md) | `DELETE /contacts/tag/delete/{id}` | [docs](https://directiq.readme.io/reference/delete_tag-delete-id) |
| [Delete Contact Lists in Bulk](actions/delete-contact-lists-in-bulk.md) | `POST /contacts/lists/delete` | [docs](https://directiq.readme.io/reference/post_lists-delete) |
| [Delete contacts from a list](actions/delete-contacts-from-a-list.md) | `POST /contacts/lists/deletecontacts/{id}` | [docs](https://directiq.readme.io/reference/post_lists-deletecontacts-id) |
| [Delete contacts from suppression list](actions/delete-contacts-from-suppression-list.md) | `POST /contacts/suppressionlist/deletecontacts` | [docs](https://directiq.readme.io/reference/post_suppressionlist-deletecontacts) |
| [Delete Contacts in Bulk](actions/delete-contacts-in-bulk.md) | `POST /contacts/contact/deletebulk` | [docs](https://directiq.readme.io/reference/post_contact-deletebulk) |
| [Delete Unused Lists in Bulk](actions/delete-unused-lists-in-bulk.md) | `DELETE /contacts/lists/deleteunusedbulk` | [docs](https://directiq.readme.io/reference/delete_lists-deleteunusedbulk) |
| [Get a contact](actions/get-a-contact.md) | `GET /contacts/contact/get/{id}` | [docs](https://directiq.readme.io/reference/get_contact-get-id) |
| [Get a contact activity](actions/get-a-contact-activity.md) | `GET /contacts/contactactivity/get/{id}` | [docs](https://directiq.readme.io/reference/get_contactactivity-get-id) |
| [Get a contact list](actions/get-a-contact-list.md) | `GET /contacts/lists/get/{id}` | [docs](https://directiq.readme.io/reference/get_lists-get-id) |
| [Get a segment](actions/get-a-segment.md) | `GET /contacts/segment/get/{id}` | [docs](https://directiq.readme.io/reference/get_segment-get-id) |
| [Get a suppression list](actions/get-a-suppression-list.md) | `GET /contacts/suppressionlist/get/{id}` | [docs](https://directiq.readme.io/reference/get_suppressionlist-get-id) |
| [Get a tag](actions/get-a-tag.md) | `GET /contacts/tag/get/{id}` | [docs](https://directiq.readme.io/reference/get_tag-get-id) |
| [Get a template](actions/get-a-template.md) | `GET /core/template/get/{id}` | [docs](https://directiq.readme.io/reference/get_template-get-id) |
| [Get bounce report](actions/get-bounce-report.md) | `GET /core/reports/bounces` | [docs](https://directiq.readme.io/reference/get_reports-bounces) |
| [Get campaign](actions/get-campaign.md) | `GET /core/campaign/get/{id}` | [docs](https://directiq.readme.io/reference/get_campaign-get-id) |
| [Get click report](actions/get-click-report.md) | `GET /core/reports/clicks` | [docs](https://directiq.readme.io/reference/get_reports-clicks) |
| [Get complaint report](actions/get-complaint-report.md) | `GET /core/reports/complaints` | [docs](https://directiq.readme.io/reference/get_reports-complaints) |
| [Get contact details](actions/get-contact-details.md) | `GET /contacts/contactdetails/get/{id}` | [docs](https://directiq.readme.io/reference/get_contactdetails-get-id) |
| [Get Document](actions/get-document.md) | `GET /core/download/{id}` | [docs](https://directiq.readme.io/reference/get_download-id) |
| [Get domain report](actions/get-domain-report.md) | `GET /core/reports/domains` | [docs](https://directiq.readme.io/reference/get_reports-domains) |
| [Get email client report](actions/get-email-client-report.md) | `GET /core/reports/emailclients` | [docs](https://directiq.readme.io/reference/get_reports-emailclients) |
| [Get number of contacts](actions/get-number-of-contacts.md) | `GET /contacts/contact/totalcount` | [docs](https://directiq.readme.io/reference/get_contact-totalcount) |
| [Get open report](actions/get-open-report.md) | `GET /core/reports/opens` | [docs](https://directiq.readme.io/reference/get_reports-opens) |
| [Get opens from social media campaign](actions/get-opens-from-social-media-campaign.md) | `GET /core/reports/socialmedia` | [docs](https://directiq.readme.io/reference/get_reports-socialmedia) |
| [Get pricing](actions/get-pricing.md) | `GET /core/pricing` | [docs](https://directiq.readme.io/reference/pricing) |
| [Get recipient report](actions/get-recipient-report.md) | `GET /core/reports/recipients` | [docs](https://directiq.readme.io/reference/get_reports-recipients) |
| [Get subscription authorization settings](actions/get-subscription-authorization-settings.md) | `GET /subscription/authorize` | [docs](https://directiq.readme.io/reference/get_authorize) |
| [Get Tag Validation](actions/get-tag-validation.md) | `POST /contacts/tag/validatetag` | [docs](https://directiq.readme.io/reference/post_tag-validatetag) |
| [Get template HTML](actions/get-template-html.md) | `GET /core/template/gethtml/{id}` | [docs](https://directiq.readme.io/reference/get_template-gethtml-id) |
| [Get unsubscribe report](actions/get-unsubscribe-report.md) | `GET /core/reports/unsubscribes` | [docs](https://directiq.readme.io/reference/get_reports-unsubscribes) |
| [List Active and Disabled Contacts](actions/list-active-and-disabled-contacts.md) | `GET /contacts/contact/getstatuscount` | [docs](https://directiq.readme.io/reference/get_contact-getstatuscount) |
| [List Campaigns](actions/list-campaigns.md) | `GET /core/campaign/list` | [docs](https://directiq.readme.io/reference/get_campaign-list) |
| [List Client Contact Keys](actions/list-client-contact-keys.md) | `GET /contacts/extradata/list` | [docs](https://directiq.readme.io/reference/get_extradata-list) |
| [List Contact Keys](actions/list-contact-keys.md) | `GET /contacts/extradata/listkeys` | [docs](https://directiq.readme.io/reference/get_extradata-listkeys) |
| [List Contact Lists](actions/list-contact-lists.md) | `GET /contacts/lists/list` | [docs](https://directiq.readme.io/reference/get_lists-list) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts/contact/list` | [docs](https://directiq.readme.io/reference/get_contact-list) |
| [List Custom Fields](actions/list-custom-fields.md) | `GET /contacts/extradata/mergetags` | [docs](https://directiq.readme.io/reference/get_extradata-mergetags) |
| [List Date Formats](actions/list-date-formats.md) | `GET /contacts/extradata/dateformats` | [docs](https://directiq.readme.io/reference/get_extradata-dateformats) |
| [List Date Keys](actions/list-date-keys.md) | `GET /contacts/extradata/listdatekeys` | [docs](https://directiq.readme.io/reference/get_extradata-listdatekeys) |
| [List Passive Contacts](actions/list-passive-contacts.md) | `GET /contacts/contact/passive` | [docs](https://directiq.readme.io/reference/get_contact-passive) |
| [List Segment Contacts](actions/list-segment-contacts.md) | `POST /contacts/segment/getcontacts` | [docs](https://directiq.readme.io/reference/post_segment-getcontacts) |
| [List Segments](actions/list-segments.md) | `GET /contacts/segment/list` | [docs](https://directiq.readme.io/reference/get_segment-list) |
| [List Segments for a Contact](actions/list-segments-for-a-contact.md) | `GET /contacts/segment/listcontactsegments` | [docs](https://directiq.readme.io/reference/get_segment-listcontactsegments) |
| [List Subscription Lists](actions/list-subscription-lists.md) | `GET /subscription/lists` | [docs](https://directiq.readme.io/reference/get_lists) |
| [List Suppression Lists](actions/list-suppression-lists.md) | `GET /contacts/suppressionlist/list` | [docs](https://directiq.readme.io/reference/get_suppressionlist-list) |
| [List Tags](actions/list-tags.md) | `GET /contacts/tag/list` | [docs](https://directiq.readme.io/reference/get_tag-list) |
| [List Templates](actions/list-templates.md) | `GET /core/template/list` | [docs](https://directiq.readme.io/reference/get_template-list) |
| [Remove a contact by email from a list](actions/remove-a-contact-by-email-from-a-list.md) | `PUT /contacts/lists/removecontactbyemail/{id}` | [docs](https://directiq.readme.io/reference/put_lists-removecontactbyemail-id) |
| [Remove a contact from a list](actions/remove-a-contact-from-a-list.md) | `PUT /contacts/lists/removecontact/{id}` | [docs](https://directiq.readme.io/reference/put_lists-removecontact-id) |
| [Remove a note from contact](actions/remove-a-note-from-contact.md) | `DELETE /contacts/contactnotes/deletenote/{id}` | [docs](https://directiq.readme.io/reference/delete_contactnotes-deletenote-id) |
| [Remove a tag from a contact using tag name and contact email](actions/remove-a-tag-from-a-contact-using-tag-name-and-contact-email.md) | `PUT /contacts/tag/removecontact` | [docs](https://directiq.readme.io/reference/put_tag-removecontact) |
| [Remove a tag from contacts](actions/remove-a-tag-from-contacts.md) | `PUT /contacts/tag/removecontacts/{id}` | [docs](https://directiq.readme.io/reference/put_tag-removecontacts-id) |
| [Remove Inactive Contacts from Lists](actions/remove-inactive-contacts-from-lists.md) | `POST /contacts/lists/sanitizelists` | [docs](https://directiq.readme.io/reference/post_lists-sanitizelists) |
| [Rename a segment](actions/rename-a-segment.md) | `PUT /contacts/segment/rename/{id}` | [docs](https://directiq.readme.io/reference/put_segment-rename-id) |
| [Rename a suppression list](actions/rename-a-suppression-list.md) | `PUT /contacts/suppressionlist/rename/{id}` | [docs](https://directiq.readme.io/reference/put_suppressionlist-rename-id) |
| [Search Contacts](actions/search-contacts.md) | `GET /contacts/contact/filter` | [docs](https://directiq.readme.io/reference/get_contact-filter) |
| [Set Contact Active](actions/set-contact-active.md) | `PUT /contacts/contact/reactivate/{id}` | [docs](https://directiq.readme.io/reference/put_contact-reactivate-id) |
| [Set Contact Disabled](actions/set-contact-disabled.md) | `POST /contacts/contact/disable` | [docs](https://directiq.readme.io/reference/post_contact-disable) |
| [Set Contacts Active in Bulk](actions/set-contacts-active-in-bulk.md) | `POST /contacts/contact/activatebulk` | [docs](https://directiq.readme.io/reference/post_contact-activatebulk) |
| [Set Contacts Disabled in Bulk](actions/set-contacts-disabled-in-bulk.md) | `POST /contacts/contact/disablebulk` | [docs](https://directiq.readme.io/reference/post_contact-disablebulk) |
| [Update a contact](actions/update-a-contact.md) | `PUT /contacts/contact/update/{id}` | [docs](https://directiq.readme.io/reference/put_contact-update-id) |
| [Update a contact list](actions/update-a-contact-list.md) | `PUT /contacts/lists/update/{id}` | [docs](https://directiq.readme.io/reference/put_lists-update-id) |
| [Update a contact note](actions/update-a-contact-note.md) | `POST /contacts/contactnotes/editnote/{id}` | [docs](https://directiq.readme.io/reference/post_contactnotes-editnote-id) |
| [Update a segment](actions/update-a-segment.md) | `PUT /contacts/segment/update/{id}` | [docs](https://directiq.readme.io/reference/put_segment-update-id) |
| [Update a tag](actions/update-a-tag.md) | `PUT /contacts/tag/update/{id}` | [docs](https://directiq.readme.io/reference/put_tag-update-id) |
| [Update Contact Details](actions/update-contact-details.md) | `POST /contacts/contactdetails/edit/{id}` | [docs](https://directiq.readme.io/reference/post_contactdetails-edit-id) |
| [Update contact key](actions/update-contact-key.md) | `PUT /contacts/extradata/update/{id}` | [docs](https://directiq.readme.io/reference/put_extradata-update-id) |
| [Update contact key visibility](actions/update-contact-key-visibility.md) | `PUT /contacts/extradata/updatekeyvisibility/{id}` | [docs](https://directiq.readme.io/reference/put_extradata-updatekeyvisibility-id) |
| [Update contact keys](actions/update-contact-keys.md) | `POST /contacts/extradata/udatekeys` | [docs](https://directiq.readme.io/reference/post_extradata-udatekeys) |
| [Update Subscription Authorization Settings](actions/update-subscription-authorization-settings.md) | `POST /subscription/authorize` | [docs](https://directiq.readme.io/reference/post_authorize) |
