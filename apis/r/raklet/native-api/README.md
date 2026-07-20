# Raklet: Native API Reference

A consolidated summary of Raklet's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://help.raklet.com/en/collections/13838830-api
- **OpenAPI specification:** https://api.raklet.com/swagger/docs/v1
- **API base URL:** `https://api.raklet.com`

## Authentication

### Password grant

Authenticate with a Raklet admin email and password to obtain a bearer token.

### Credentials

- **Username:** `username` · required · Your Raklet admin email address.
- **Password:** `password` · required · Your Raklet admin password.
- **Organisation ID:** `organisationId` · required · Your Raklet organisation ID from Admin settings.

Send these headers with each API request:

```http
Authorization: Bearer <custom.accessToken>
```

[Official authentication documentation](https://help.raklet.com/en/articles/11728820-how-to-authenticate-with-the-raklet-api)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `pageSize` in the query string to set the page size. Use `offset` in the query string as the record offset.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Contact Address](actions/add-contact-address.md) | `POST /organisations/:organisationId/contacts/:organisationMembershipId/addresses` | [docs](https://api.raklet.com/swagger/ui/index#/ContactAddress/ContactAddress_Post) |
| [Add Contact Email](actions/add-contact-email.md) | `POST /organisations/:organisationId/contacts/:organisationMembershipId/emails` | [docs](https://api.raklet.com/swagger/ui/index#/ContactEmail/ContactEmail_Post) |
| [Add Contact Phone](actions/add-contact-phone.md) | `POST /organisations/:organisationId/contacts/:organisationMembershipId/phones` | [docs](https://api.raklet.com/swagger/ui/index#/ContactPhone/ContactPhone_Post) |
| [Authenticate](actions/authenticate.md) | `POST /token` | [docs](https://help.raklet.com/en/articles/11728820-how-to-authenticate-with-the-raklet-api) |
| [Create Contact](actions/create-contact.md) | `POST /organisations/:organisationId/contacts` | [docs](https://api.raklet.com/swagger/ui/index#/Contact/Contact_Post) |
| [Create Debt](actions/create-debt.md) | `POST /organisations/:organisationId/debts` | [docs](https://api.raklet.com/swagger/ui/index#/AdminDebts/AdminDebts_PostDebts) |
| [Create Donation](actions/create-donation.md) | `POST /organisations/:organisationId/donations` | [docs](https://api.raklet.com/swagger/ui/index#/AdminDonations/AdminDonations_PostDonations) |
| [Create Payment](actions/create-payment.md) | `POST /organisations/:organisationId/payments` | [docs](https://api.raklet.com/swagger/ui/index#/AdminPayments/AdminPayments_PostPayments) |
| [Create Post](actions/create-post.md) | `POST /organisations/:organisationId/posts` | [docs](https://api.raklet.com/swagger/ui/index#/Posts/Posts_CreatePost) |
| [Create Subscription](actions/create-subscription.md) | `POST /organisations/:organisationId/subscriptions` | [docs](https://api.raklet.com/swagger/ui/index#/Subscription/Subscription_AddSubscription) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /organisations/:organisationId/contacts/:organisationMembershipId` | [docs](https://api.raklet.com/swagger/ui/index#/Contact/Contact_Delete) |
| [Delete Contact Address](actions/delete-contact-address.md) | `DELETE /organisations/:organisationId/contacts/:organisationMembershipId/addresses/:id` | [docs](https://api.raklet.com/swagger/ui/index#/ContactAddress/ContactAddress_Delete) |
| [Delete Contact Email](actions/delete-contact-email.md) | `DELETE /organisations/:organisationId/contacts/:organisationMembershipId/emails/:id` | [docs](https://api.raklet.com/swagger/ui/index#/ContactEmail/ContactEmail_Delete) |
| [Delete Contact Phone](actions/delete-contact-phone.md) | `DELETE /organisations/:organisationId/contacts/:organisationMembershipId/phones/:id` | [docs](https://api.raklet.com/swagger/ui/index#/ContactPhone/ContactPhone_Delete) |
| [Delete Subscription](actions/delete-subscription.md) | `DELETE /organisations/:organisationId/subscriptions/:subscriptionId` | [docs](https://api.raklet.com/swagger/ui/index#/Subscription/Subscription_DeleteSubscription) |
| [Get Contact Details](actions/get-contact-details.md) | `GET /organisations/:organisationId/contacts/:organisationMembershipId/details` | [docs](https://api.raklet.com/swagger/ui/index#/Contact/Contact_GetDetails) |
| [Get Debt](actions/get-debt.md) | `GET /organisations/:organisationId/debts/:id` | [docs](https://api.raklet.com/swagger/ui/index#/AdminDebts/AdminDebts_GetDebt) |
| [Get Donation](actions/get-donation.md) | `GET /organisations/:organisationId/donations/:id` | [docs](https://api.raklet.com/swagger/ui/index#/AdminDonations/AdminDonations_GetDonation) |
| [Get Event](actions/get-event.md) | `GET /app/organisations/:organisationId/events/:id` | [docs](https://api.raklet.com/swagger/ui/index#/Events/Events_GetEvent) |
| [Get organisation settings](actions/get-organisation-settings.md) | `GET /app/organisations/:organisationId/settings` | [docs](https://help.raklet.com/en/articles/11728891-make-your-first-api-call) |
| [Get Payment](actions/get-payment.md) | `GET /organisations/:organisationId/payments/:id` | [docs](https://api.raklet.com/swagger/ui/index#/AdminPayments/AdminPayments_GetAdminPayment) |
| [Get Plan](actions/get-plan.md) | `GET /organisations/:organisationId/plans/:id` | [docs](https://api.raklet.com/swagger/ui/index#/AdminPlans/AdminPlans_GetPlan) |
| [Get Subscription](actions/get-subscription.md) | `GET /organisations/:organisationId/subscriptions/:subscriptionId` | [docs](https://api.raklet.com/swagger/ui/index#/Subscription/Subscription_GetSubscriptionById) |
| [List Boards](actions/list-boards.md) | `GET /organisations/:organisationId/boards` | [docs](https://api.raklet.com/swagger/ui/index#/Boards/Boards_GetList) |
| [List Contacts](actions/list-contacts.md) | `GET /organisations/:organisationId/contacts` | [docs](https://api.raklet.com/swagger/ui/index#/Contact/Contact_GetContacts) |
| [List Debts](actions/list-debts.md) | `GET /organisations/:organisationId/debts` | [docs](https://api.raklet.com/swagger/ui/index#/AdminDebts/AdminDebts_GetDebts) |
| [List Donations](actions/list-donations.md) | `GET /organisations/:organisationId/donations` | [docs](https://api.raklet.com/swagger/ui/index#/AdminDonations/AdminDonations_GetDonations) |
| [List Events](actions/list-events.md) | `GET /app/organisations/:organisationId/events` | [docs](https://api.raklet.com/swagger/ui/index#/Events/Events_GetEvents) |
| [List Payments](actions/list-payments.md) | `GET /organisations/:organisationId/payments` | [docs](https://api.raklet.com/swagger/ui/index#/AdminPayments/AdminPayments_GetPayments) |
| [List Plans](actions/list-plans.md) | `GET /organisations/:organisationId/plans` | [docs](https://api.raklet.com/swagger/ui/index#/AdminPlans/AdminPlans_GetPlans) |
| [List Posts](actions/list-posts.md) | `GET /organisations/:organisationId/posts` | [docs](https://api.raklet.com/swagger/ui/index#/Posts/Posts_GetPosts) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET /organisations/:organisationId/subscriptions` | [docs](https://api.raklet.com/swagger/ui/index#/Subscription/Subscription_GetSubscriptions) |
| [Set Primary Contact Address](actions/set-primary-contact-address.md) | `PATCH /organisations/:organisationId/contacts/:organisationMembershipId/addresses/:id/SetPrimary` | [docs](https://api.raklet.com/swagger/ui/index#/ContactAddress/ContactAddress_SetPrimary) |
| [Set Primary Contact Email](actions/set-primary-contact-email.md) | `PATCH /organisations/:organisationId/contacts/:organisationMembershipId/emails/:id/SetPrimary` | [docs](https://api.raklet.com/swagger/ui/index#/ContactEmail/ContactEmail_SetPrimary) |
| [Set Primary Contact Phone](actions/set-primary-contact-phone.md) | `PATCH /organisations/:organisationId/contacts/:organisationMembershipId/phones/:id/SetPrimary` | [docs](https://api.raklet.com/swagger/ui/index#/ContactPhone/ContactPhone_SetPrimary) |
| [Update Contact](actions/update-contact.md) | `PUT /organisations/:organisationId/contacts/:organisationMembershipId` | [docs](https://api.raklet.com/swagger/ui/index#/Contact/Contact_Put) |
| [Update Contact Address](actions/update-contact-address.md) | `PUT /organisations/:organisationId/contacts/:organisationMembershipId/addresses/:id` | [docs](https://api.raklet.com/swagger/ui/index#/ContactAddress/ContactAddress_Put) |
| [Update Contact Email](actions/update-contact-email.md) | `PUT /organisations/:organisationId/contacts/:organisationMembershipId/emails/:id` | [docs](https://api.raklet.com/swagger/ui/index#/ContactEmail/ContactEmail_Put) |
| [Update Contact Phone](actions/update-contact-phone.md) | `PUT /organisations/:organisationId/contacts/:organisationMembershipId/phones/:id` | [docs](https://api.raklet.com/swagger/ui/index#/ContactPhone/ContactPhone_Put) |
| [Update Subscription](actions/update-subscription.md) | `PUT /organisations/:organisationId/subscriptions/:subscriptionId` | [docs](https://api.raklet.com/swagger/ui/index#/Subscription/Subscription_UpdateSubscription) |
