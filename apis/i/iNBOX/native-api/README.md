# INBOX: Native API Reference

A consolidated summary of INBOX's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://reference.useinbox.com/
- **API base URL:** `https://useapi.useinbox.com`

## Authentication

### Basic

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

[Official authentication documentation](https://developers.useinbox.com/)

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Single Contact To List](actions/add-single-contact-to-list.md) | `POST /inbox/v1/contactlists/:id/add` | [docs](https://reference.useinbox.com/) |
| [Change Contact Status](actions/change-contact-status.md) | `PATCH /inbox/v1/contacts/:id/status` | [docs](https://reference.useinbox.com/) |
| [Create Campaign With Custom HTML](actions/create-campaign-with-custom-html.md) | `POST /inbox/v1/campaigns/custom` | [docs](https://reference.useinbox.com/) |
| [Create Campaign With Newsletter](actions/create-campaign-with-newsletter.md) | `POST /inbox/v1/campaigns` | [docs](https://reference.useinbox.com/) |
| [Create Contact List](actions/create-contact-list.md) | `POST /inbox/v1/contactlists` | [docs](https://reference.useinbox.com/) |
| [Create Custom Field](actions/create-custom-field.md) | `POST /inbox/v1/customfields` | [docs](https://reference.useinbox.com/) |
| [Create Group](actions/create-group.md) | `POST /inbox/v1/groups` | [docs](https://reference.useinbox.com/) |
| [Create Newsletter](actions/create-newsletter.md) | `POST /inbox/v1/newsletters` | [docs](https://reference.useinbox.com/) |
| [Create Sender](actions/create-sender.md) | `POST /inbox/v1/senders` | [docs](https://reference.useinbox.com/) |
| [Delete Contact List](actions/delete-contact-list.md) | `DELETE /inbox/v1/contactlists/:id` | [docs](https://reference.useinbox.com/) |
| [Delete Custom Field](actions/delete-custom-field.md) | `DELETE /inbox/v1/customfields/:id` | [docs](https://reference.useinbox.com/) |
| [Delete Groups](actions/delete-groups.md) | `DELETE /inbox/v1/groups/:id` | [docs](https://reference.useinbox.com/) |
| [Delete Newsletter](actions/delete-newsletter.md) | `DELETE /inbox/v1/newsletters/:id` | [docs](https://reference.useinbox.com/) |
| [Delete Segment](actions/delete-segment.md) | `DELETE /inbox/v1/segments/:id` | [docs](https://reference.useinbox.com/) |
| [Delete Sender](actions/delete-sender.md) | `DELETE /inbox/v1/senders/:id` | [docs](https://reference.useinbox.com/) |
| [Delete Single Contact From List](actions/delete-single-contact-from-list.md) | `DELETE /inbox/v1/contactlists/:id/delete/:contact-id` | [docs](https://reference.useinbox.com/) |
| [Get All Campaigns](actions/get-all-campaigns.md) | `GET /inbox/v1/campaigns` | [docs](https://reference.useinbox.com/) |
| [Get All Contact Lists](actions/get-all-contact-lists.md) | `GET /inbox/v1/contactlists` | [docs](https://reference.useinbox.com/) |
| [Get All Contacts](actions/get-all-contacts.md) | `GET /inbox/v1/contacts` | [docs](https://reference.useinbox.com/) |
| [Get All Custom Fields](actions/get-all-custom-fields.md) | `GET /inbox/v1/customfields` | [docs](https://reference.useinbox.com/) |
| [Get All Groups](actions/get-all-groups.md) | `GET /inbox/v1/groups` | [docs](https://reference.useinbox.com/) |
| [Get All Newsletters](actions/get-all-newsletters.md) | `GET /inbox/v1/newsletters` | [docs](https://reference.useinbox.com/) |
| [Get All Segments](actions/get-all-segments.md) | `GET /inbox/v1/segments` | [docs](https://reference.useinbox.com/) |
| [Get All Senders](actions/get-all-senders.md) | `GET /inbox/v1/senders` | [docs](https://reference.useinbox.com/) |
| [Get Campaign](actions/get-campaign.md) | `GET /inbox/v1/campaigns/:id` | [docs](https://reference.useinbox.com/) |
| [Get Contact](actions/get-contact.md) | `GET /inbox/v1/contacts/:id` | [docs](https://reference.useinbox.com/) |
| [Get Import Status](actions/get-import-status.md) | `GET /inbox/v1/contactlists/:contactListId/import/:importId` | [docs](https://reference.useinbox.com/) |
| [Get Newsletter](actions/get-newsletter.md) | `GET /inbox/v1/newsletters/:id` | [docs](https://reference.useinbox.com/) |
| [Import Contacts To List](actions/import-contacts-to-list.md) | `POST /inbox/v1/contactlists/:contactlistId/import` | [docs](https://reference.useinbox.com/) |
| [Replace Contact List](actions/replace-contact-list.md) | `PUT /inbox/v1/contactlists/:id` | [docs](https://reference.useinbox.com/) |
| [Replace Custom Field](actions/replace-custom-field.md) | `PUT /inbox/v1/customfields/:id` | [docs](https://reference.useinbox.com/) |
| [Replace Group](actions/replace-group.md) | `PUT /inbox/v1/groups/:id` | [docs](https://reference.useinbox.com/) |
| [Replace Newsletter](actions/replace-newsletter.md) | `PUT /inbox/v1/newsletters/:id` | [docs](https://reference.useinbox.com/) |
| [Replace Sender](actions/replace-sender.md) | `PUT /inbox/v1/senders/:id` | [docs](https://reference.useinbox.com/) |
| [Update Contact](actions/update-contact.md) | `POST /inbox/v1/contacts/:id` | [docs](https://reference.useinbox.com/) |
| [Update Contact List](actions/update-contact-list.md) | `PATCH /inbox/v1/contactlists/:id` | [docs](https://reference.useinbox.com/) |
| [Update Custom Field](actions/update-custom-field.md) | `PATCH /inbox/v1/customfields/:id` | [docs](https://reference.useinbox.com/) |
| [Update Groups](actions/update-groups.md) | `PATCH /inbox/v1/groups/:id` | [docs](https://reference.useinbox.com/) |
| [Update Newsletter](actions/update-newsletter.md) | `PATCH /inbox/v1/newsletters/:id` | [docs](https://reference.useinbox.com/) |
| [Update Sender](actions/update-sender.md) | `PATCH /inbox/v1/senders/:id` | [docs](https://reference.useinbox.com/) |
