# Dynosend: Native API Reference

A consolidated summary of Dynosend's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://developers.dynosend.com/
- **API base URL:** `https://api.dynosend.com/api/v2`

## Authentication

### API Token

Authenticate Dynosend requests with a bearer API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.dynosend.com/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 20). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Contact Tags by Email](actions/add-contact-tags-by-email.md) | `PATCH /contacts/addtag` | [docs](https://developers.dynosend.com/#tagacontact) |
| [Add Contact Tags by UID](actions/add-contact-tags-by-uid.md) | `PATCH /contacts/addtag` | [docs](https://developers.dynosend.com/#tagacontact) |
| [Add to Blacklist](actions/add-to-blacklist.md) | `POST /blacklist/add` | [docs](https://developers.dynosend.com/#addtoblacklist) |
| [Check Blacklist](actions/check-blacklist.md) | `POST /blacklist` | [docs](https://developers.dynosend.com/#checkacontact) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://developers.dynosend.com/#createacontact) |
| [Create Contact and Ignore Double Opt-In](actions/create-contact-ignore-double-opt-in.md) | `POST /contacts` | [docs](https://developers.dynosend.com/#createacontact) |
| [Delete Contact by Email](actions/delete-contact-by-email.md) | `DELETE /contacts` | [docs](https://developers.dynosend.com/#deleteacontact) |
| [Delete Contact by UID](actions/delete-contact-by-uid.md) | `DELETE /contacts` | [docs](https://developers.dynosend.com/#deleteacontact) |
| [Find Duplicate Contacts by Email](actions/find-duplicate-contacts-by-email.md) | `GET /contacts/duplicate` | [docs](https://developers.dynosend.com/#getaduplicatecontact) |
| [Get Audience](actions/get-audience.md) | `GET /audiences` | [docs](https://developers.dynosend.com/#getanaudience) |
| [Get Campaign](actions/get-campaign.md) | `GET /campaigns` | [docs](https://developers.dynosend.com/#getacampaign) |
| [Get Contact by Email](actions/get-contact-by-email.md) | `GET /contacts` | [docs](https://developers.dynosend.com/#getacontact) |
| [Get Contact by UID](actions/get-contact-by-uid.md) | `GET /contacts` | [docs](https://developers.dynosend.com/#getacontact) |
| [List Audiences](actions/list-audiences.md) | `GET /audiences` | [docs](https://developers.dynosend.com/#listaudiences) |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaigns` | [docs](https://developers.dynosend.com/#listcampaign) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://developers.dynosend.com/#listcontacts) |
| [Pause Campaign](actions/pause-campaign.md) | `POST /campaigns/pause` | [docs](https://developers.dynosend.com/#pauseacampaign) |
| [Register Push Device by Contact UID](actions/register-push-device-by-contact-uid.md) | `POST https://api.dynosend.com/device/register` | [docs](https://docs.dynosend.com/a-21-firebase-cloud-messaging-fcm-setup-for-push-notifications) |
| [Register Push Device by Email](actions/register-push-device-by-email.md) | `POST https://api.dynosend.com/device/register` | [docs](https://docs.dynosend.com/a-21-firebase-cloud-messaging-fcm-setup-for-push-notifications) |
| [Resume Campaign](actions/resume-campaign.md) | `POST /campaigns/resume` | [docs](https://developers.dynosend.com/#resumeacampaign) |
| [Send Contact Event by Email](actions/send-contact-event-by-email.md) | `POST /events` | [docs](https://developers.dynosend.com/#sendanevent) |
| [Send Contact Event by UID](actions/send-contact-event-by-uid.md) | `POST /events` | [docs](https://developers.dynosend.com/#sendanevent) |
| [Send Transactional Message](actions/send-transactional-message.md) | `POST /transactional` | [docs](https://developers.dynosend.com/#sendamessage) |
| [Send Transactional Message with External Content](actions/send-transactional-message-with-external-content.md) | `POST /transactional` | [docs](https://developers.dynosend.com/#sendamessage) |
| [Start Campaign](actions/start-campaign.md) | `POST /campaigns/start` | [docs](https://developers.dynosend.com/#startacampaign) |
| [Subscribe Contact by Email](actions/subscribe-contact-by-email.md) | `PATCH /contacts/subscribe` | [docs](https://developers.dynosend.com/#subscribeacontact) |
| [Subscribe Contact by UID](actions/subscribe-contact-by-uid.md) | `PATCH /contacts/subscribe` | [docs](https://developers.dynosend.com/#subscribeacontact) |
| [Unsubscribe Contact by Email](actions/unsubscribe-contact-by-email.md) | `PATCH /contacts/unsubscribe` | [docs](https://developers.dynosend.com/#unsubscribeacontact) |
| [Unsubscribe Contact by UID](actions/unsubscribe-contact-by-uid.md) | `PATCH /contacts/unsubscribe` | [docs](https://developers.dynosend.com/#unsubscribeacontact) |
| [Update Contact by Email](actions/update-contact-by-email.md) | `PATCH /contacts/update` | [docs](https://developers.dynosend.com/#updateacontact) |
| [Update Contact by UID](actions/update-contact-by-uid.md) | `PATCH /contacts/update` | [docs](https://developers.dynosend.com/#updateacontact) |
