# Explara: Native API Reference

A consolidated summary of Explara's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://apidocs.explara.com/
- **API base URL:** `https://www.explara.com`

## Authentication

### OAuth2

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://www.explara.com/a/account/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://www.explara.com/a/account/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


[Official authentication documentation](https://developers.explara.com/get-api-access)

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Account Profile](actions/account-profile.md) | `GET /a/api/web/profile` | [docs](https://apidocs.explara.com/) |
| [Attendee Form](actions/attendee-form.md) | `POST /api/publisher/attendee-form` | [docs](https://apidocs.explara.com/) |
| [Edit Member Form](actions/edit-member-form.md) | `POST /cm/api/publisher/edit-membership-form` | [docs](https://apidocs.explara.com/) |
| [Event Cart Calculation](actions/event-cart-calculation.md) | `POST /api/publisher/cart-calculation` | [docs](https://apidocs.explara.com/) |
| [Event Generate Order](actions/event-generate-order.md) | `POST /api/publisher/generate-order` | [docs](https://apidocs.explara.com/) |
| [Get Event Details](actions/get-event-details.md) | `POST /api/resource/event-detail` | [docs](https://apidocs.explara.com/) |
| [Get Event Report](actions/get-event-report.md) | `POST /api/e/get-report` | [docs](https://developers.explara.com/developers-api#10-get-event-report) |
| [Group Members](actions/group-members.md) | `POST /cm/api/publisher/members` | [docs](https://apidocs.explara.com/) |
| [List Event Attendees](actions/list-event-attendees.md) | `POST /api/e/attendee-list` | [docs](https://developers.explara.com/developers-api#11-event-attendee-list) |
| [List Events](actions/list-events.md) | `POST /api/e/get-all-events` | [docs](https://developers.explara.com/developers-api#9-get-event-list) |
| [List Groups](actions/list-groups.md) | `GET /cm/api/publisher/list` | [docs](https://apidocs.explara.com/) |
| [List Tickets](actions/list-tickets.md) | `POST /api/publisher/ticket-details` | [docs](https://apidocs.explara.com/) |
| [Member Profile](actions/member-profile.md) | `POST /cm/api/publisher/public-profile` | [docs](https://apidocs.explara.com/) |
| [Membership Form](actions/membership-form.md) | `POST /cm/api/membership/membership-form` | [docs](https://apidocs.explara.com/) |
| [Membership Generate Cart](actions/membership-generate-cart.md) | `POST /cm/api/membership/generate-cart` | [docs](https://apidocs.explara.com/) |
| [Membership Members Details](actions/membership-members-details.md) | `POST /cm/api/membership/members-details` | [docs](https://apidocs.explara.com/) |
| [Membership Order Details](actions/membership-order-details.md) | `POST /cm/api/membership/order-details` | [docs](https://apidocs.explara.com/) |
| [My Membership](actions/my-membership.md) | `POST /cm/api/publisher/my-membership` | [docs](https://apidocs.explara.com/) |
| [Order Details](actions/order-details.md) | `POST /api/publisher/order-details` | [docs](https://apidocs.explara.com/) |
| [Search Group Members](actions/search-group-members.md) | `POST /cm/api/publisher/search-members` | [docs](https://apidocs.explara.com/) |
