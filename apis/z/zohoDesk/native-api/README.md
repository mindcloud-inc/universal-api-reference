# Zoho Desk: Native API Reference

A consolidated summary of Zoho Desk's API configuration and 27 documented operations, with links to official documentation.

- **Official docs:** https://desk.zoho.com/DeskAPIDocument
- **API base URL:** `https://desk.zoho.com/api/v1`

## Authentication

### OAuth 2.0

Zoho OAuth 2.0 for Zoho Desk

### Credentials

- **Accounts Server:** `accountsServer` · optional · Zoho Accounts base URL for your Desk data center. Use the exact Accounts URL from Zoho's Multi-DC support page, such as https://accounts.zoho.com or https://accounts.zoho.eu.
- **Organization ID:** `orgId` · required · This app requires a Zoho Organization ID. Choose the organization you want to work with before connecting. You can find it in Settings>Developer>API

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to {{credentials.accountsServer}}/oauth/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to {{credentials.accountsServer}}/oauth/v2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `Desk.basic.READ,Desk.settings.READ,Desk.tickets.ALL,Desk.search.READ,Desk.contacts.READ,Desk.contacts.WRITE,Desk.contacts.CREATE,Desk.contacts.UPDATE,Desk.events.ALL,Desk.departments.READ`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to {{credentials.accountsServer}}/oauth/v2/token.

[Official authentication documentation](https://desk.zoho.com/DeskAPIDocument#OauthTokens)

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–100). Use `from` in the query string as the record offset; numbering starts at 0.

## Endpoints (27 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Account](actions/create-account.md) | `POST /accounts` | [docs](https://github.com/zoho/zohodesk-oas/blob/master/v1.0/Account.json) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://github.com/zoho/zohodesk-oas/blob/master/v1.0/Contact.json) |
| [Create Ticket](actions/create-ticket.md) | `POST /tickets` | [docs](https://github.com/zoho/zohodesk-oas/blob/master/v1.0/Ticket.json) |
| [Create Ticket Comment](actions/create-ticket-comment.md) | `POST /tickets/[:ticketId]/comments` | [docs](https://github.com/zoho/zohodesk-oas/blob/master/v1.0/TicketComment.json) |
| [Get Account](actions/get-account.md) | `GET /accounts/[:accountId]` | [docs](https://github.com/zoho/zohodesk-oas/blob/master/v1.0/Account.json) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/[:contactId]` | [docs](https://github.com/zoho/zohodesk-oas/blob/master/v1.0/Contact.json) |
| [Get Department](actions/get-department.md) | `GET /departments/[:departmentId]` | [docs](https://github.com/zoho/zohodesk-oas/blob/master/v1.0/Department.json) |
| [Get My Profile](actions/get-my-profile.md) | `GET myProfile` | [docs](https://desk.zoho.com/DeskAPIDocument#Profiles_Getmyprofiledetails) |
| [Get Ticket](actions/get-ticket.md) | `GET /tickets/[:ticketId]` | [docs](https://github.com/zoho/zohodesk-oas/blob/master/v1.0/Ticket.json) |
| [List Accounts](actions/list-accounts.md) | `GET /accounts` | [docs](https://github.com/zoho/zohodesk-oas/blob/master/v1.0/Account.json) |
| [List Channels](actions/list-channels.md) | `GET /channels` | [docs](https://desk.zoho.com/DeskAPIDocument#Channels#Channels_Listconfiguredchannels) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://github.com/zoho/zohodesk-oas/blob/master/v1.0/Contact.json) |
| [List Departments](actions/list-departments.md) | `GET /departments` | [docs](https://github.com/zoho/zohodesk-oas/blob/master/v1.0/Department.json) |
| [List Layouts](actions/list-layouts.md) | `GET layouts` | [docs](https://desk.zoho.com/DeskAPIDocument#Layouts#Layouts_ListLayouts) |
| [List Organization Fields In Module](actions/list-organization-fields-in-module.md) | `GET /organizationFields` | [docs](https://github.com/zoho/zohodesk-oas/blob/master/v1.0/Field.json) |
| [List Organizations](actions/list-organizations.md) | `GET /organizations` | [docs](https://desk.zoho.com/DeskAPIDocument#Organizations_Getallorganizations) |
| [List Threads](actions/list-threads.md) | `GET /tickets/[:ticketId]/threads` | [docs](https://github.com/zoho/zohodesk-oas/blob/master/v1.0/Thread.json) |
| [List Ticket Comments](actions/list-ticket-comments.md) | `GET /tickets/[:ticketId]/comments` | [docs](https://github.com/zoho/zohodesk-oas/blob/master/v1.0/TicketComment.json) |
| [List Tickets](actions/list-tickets.md) | `GET /tickets` | [docs](https://github.com/zoho/zohodesk-oas/blob/master/v1.0/Ticket.json) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://github.com/zoho/zohodesk-oas/blob/master/v1.0/Webhook.json) |
| [Move Ticket](actions/move-ticket.md) | `POST /tickets/[:ticketId]/move` | [docs](https://github.com/zoho/zohodesk-oas/blob/master/v1.0/Ticket.json) |
| [Search Accounts](actions/search-accounts.md) | `GET /accounts/search` | [docs](https://github.com/zoho/zohodesk-oas/blob/master/v1.0/Search.json) |
| [Search Contacts](actions/search-contacts.md) | `GET /contacts/search` | [docs](https://github.com/zoho/zohodesk-oas/blob/master/v1.0/Search.json) |
| [Search Tickets](actions/search-tickets.md) | `GET /tickets/search` | [docs](https://github.com/zoho/zohodesk-oas/blob/master/v1.0/Search.json) |
| [Update Account](actions/update-account.md) | `PATCH /accounts/[:accountId]` | [docs](https://github.com/zoho/zohodesk-oas/blob/master/v1.0/Account.json) |
| [Update Contact](actions/update-contact.md) | `PATCH /contacts/[:contactId]` | [docs](https://github.com/zoho/zohodesk-oas/blob/master/v1.0/Contact.json) |
| [Update Ticket](actions/update-ticket.md) | `PATCH /tickets/[:ticketId]` | [docs](https://github.com/zoho/zohodesk-oas/blob/master/v1.0/Ticket.json) |
