# UseINBOX: Native API Reference

A consolidated summary of UseINBOX's API configuration and 41 documented operations, with links to official documentation.

- **Official docs:** https://developers.useinbox.com/
- **API base URL:** `https://useapi.useinbox.com`

## Authentication

### INBOX Account

Authenticate with an INBOX account email and password. The connector exchanges these credentials for a short-lived bearer token through POST /token.

### Credentials

- **Email Address:** `emailAddress` · required · INBOX account email address used to request bearer tokens from POST /token.
- **Password:** `password` · required · INBOX account password used to request bearer tokens from POST /token.

Send these headers with each API request:

```http
Authorization: Bearer <custom.access_token>
```

[Official authentication documentation](https://developers.useinbox.com/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (41 documented)

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
| [Delete Group](actions/delete-group.md) | `DELETE /inbox/v1/groups/:id` | [docs](https://reference.useinbox.com/) |
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
| [Get Contact Import Status](actions/get-contact-import-status.md) | `GET /inbox/v1/contactlists/:contactListId/import/:importId` | [docs](https://reference.useinbox.com/) |
| [Get Newsletter](actions/get-newsletter.md) | `GET /inbox/v1/newsletters/:id` | [docs](https://reference.useinbox.com/) |
| [Get Token](actions/get-token.md) | `POST /token` | [docs](https://developers.useinbox.com/) |
| [Import Contacts To List](actions/import-contacts-to-list.md) | `POST /inbox/v1/contactlists/:contactlistId/import` | [docs](https://reference.useinbox.com/) |
| [Replace Contact List](actions/replace-contact-list.md) | `PUT /inbox/v1/contactlists/:id` | [docs](https://reference.useinbox.com/) |
| [Replace Custom Field](actions/replace-custom-field.md) | `PUT /inbox/v1/customfields/:id` | [docs](https://reference.useinbox.com/) |
| [Replace Group](actions/replace-group.md) | `PUT /inbox/v1/groups/:id` | [docs](https://reference.useinbox.com/) |
| [Replace Newsletter](actions/replace-newsletter.md) | `PUT /inbox/v1/newsletters/:id` | [docs](https://reference.useinbox.com/) |
| [Replace Sender](actions/replace-sender.md) | `PUT /inbox/v1/senders/:id` | [docs](https://reference.useinbox.com/) |
| [Update Contact](actions/update-contact.md) | `POST /inbox/v1/contacts/:id` | [docs](https://reference.useinbox.com/) |
| [Update Contact List](actions/update-contact-list.md) | `PATCH /inbox/v1/contactlists/:id` | [docs](https://reference.useinbox.com/) |
| [Update Custom Field](actions/update-custom-field.md) | `PATCH /inbox/v1/customfields/:id` | [docs](https://reference.useinbox.com/) |
| [Update Group](actions/update-group.md) | `PATCH /inbox/v1/groups/:id` | [docs](https://reference.useinbox.com/) |
| [Update Newsletter](actions/update-newsletter.md) | `PATCH /inbox/v1/newsletters/:id` | [docs](https://reference.useinbox.com/) |
| [Update Sender](actions/update-sender.md) | `PATCH /inbox/v1/senders/:id` | [docs](https://reference.useinbox.com/) |
