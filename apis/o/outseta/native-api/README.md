# Outseta: Native API Reference

A consolidated summary of Outseta's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k
- **API base URL:** `https://{subdomain}.outseta.com/api/v1`

## Authentication

### API Key

Connect with your Outseta API key, secret key, and tenant subdomain.

### Credentials

- **API Key:** `apiKey` · required
- **Subdomain:** `subdomain` · required · Your Outseta subdomain, for example acme in acme.outseta.com.
- **Secret Key:** `secretKey` · required · The Outseta API secret key paired with your API key.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k#intro)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–100). Use `offset` in the query string to choose the page; numbering starts at 0.

## Sorting

Set the sort field with `orderBy` in the query string. Use `ASC` for ascending order and `DESC` for descending order. Only one sort field is accepted.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Account with Existing Person](actions/add-account-with-existing-person.md) | `POST /crm/accounts` | [docs](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k) |
| [Add Account with New Person](actions/add-account-with-new-person.md) | `POST /crm/accounts` | [docs](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k) |
| [Add Account with Subscription](actions/add-account-with-subscription.md) | `POST /crm/accounts` | [docs](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k) |
| [Add Add-On to Subscription](actions/add-add-on-to-subscription.md) | `POST /billing/subscriptionaddons` | [docs](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k) |
| [Add Custom Activity](actions/add-custom-activity.md) | `POST /activities/customactivity` | [docs](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k) |
| [Add Deal](actions/add-deal.md) | `POST /crm/deals` | [docs](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k) |
| [Add Discount to Subscription](actions/add-discount-to-subscription.md) | `POST /billing/subscriptions/:subscriptionUid/discounts/:discountUid` | [docs](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k) |
| [Add Existing Person to Existing Account](actions/add-existing-person-to-existing-account.md) | `POST /crm/accounts/:accountUid/memberships` | [docs](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k) |
| [Add First Time Subscription](actions/add-first-time-subscription.md) | `PUT /billing/subscriptions/firsttimesubscription` | [docs](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k) |
| [Add First Time Subscription Preview](actions/add-first-time-subscription-preview.md) | `POST /billing/subscriptions/compute-charge-summary` | [docs](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k) |
| [Add Invoice Payment](actions/add-invoice-payment.md) | `POST /billing/transactions/payment` | [docs](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k) |
| [Add New Invoice](actions/add-new-invoice.md) | `POST /billing/invoices` | [docs](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k) |
| [Add New Person to Existing Account](actions/add-new-person-to-existing-account.md) | `POST /crm/accounts/:accountUid/memberships` | [docs](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k) |
| [Add Person](actions/add-person.md) | `POST /crm/people` | [docs](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k) |
| [Cancel Account](actions/cancel-account.md) | `PUT /crm/accounts/cancellation/:accountUid` | [docs](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k) |
| [Change Subscription](actions/change-subscription.md) | `PUT /billing/subscriptions/:subscriptionUid/changesubscription` | [docs](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k) |
| [Change Subscription Preview](actions/change-subscription-preview.md) | `PUT /billing/subscriptions/:subscriptionUid/changesubscriptionpreview` | [docs](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k) |
| [Delete Deal](actions/delete-deal.md) | `DELETE /crm/deals/:dealUid` | [docs](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k) |
| [Delete Person](actions/delete-person.md) | `DELETE /crm/people/:personUid` | [docs](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k) |
| [Extend Trial Subscription](actions/extend-trial-subscription.md) | `PUT /crm/accounts/extendtrial/:accountUid/:date` | [docs](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k) |
| [Get Account](actions/get-account.md) | `GET /crm/accounts/:accountUid` | [docs](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k) |
| [Get Deal](actions/get-deal.md) | `GET /crm/deals/:dealUid` | [docs](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k) |
| [Get Person](actions/get-person.md) | `GET /crm/people/:personUid` | [docs](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k) |
| [Get Subscription](actions/get-subscription.md) | `GET /billing/subscriptions/:subscriptionUid` | [docs](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k) |
| [Initiate Password Reset](actions/initiate-password-reset.md) | `POST /crm/people/forgotPassword` | [docs](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k) |
| [List Accounts](actions/list-accounts.md) | `GET /crm/accounts` | [docs](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k) |
| [List Activities](actions/list-activities.md) | `GET /activities` | [docs](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k) |
| [List Deals](actions/list-deals.md) | `GET /crm/deals` | [docs](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k) |
| [List People](actions/list-people.md) | `GET /crm/people` | [docs](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k) |
| [List Plan Families](actions/list-plan-families.md) | `GET /billing/planfamilies` | [docs](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k) |
| [List Plans](actions/list-plans.md) | `GET /billing/plans` | [docs](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k) |
| [List Transactions by Account](actions/list-transactions-by-account.md) | `GET /billing/transactions/:accountUid` | [docs](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k) |
| [Register Account](actions/register-account.md) | `POST /crm/registrations` | [docs](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k) |
| [Remove Cancellation](actions/remove-cancellation.md) | `PUT /crm/accounts/removecancellation/:accountUid` | [docs](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k) |
| [Remove Person from Account](actions/remove-person-from-account.md) | `DELETE /crm/accounts/:accountUid/memberships/:membershipUid` | [docs](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k) |
| [Set Temporary Password](actions/set-temporary-password.md) | `PUT /crm/people/:personUid/setTemporaryPassword` | [docs](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k) |
| [Update Account](actions/update-account.md) | `PUT /crm/accounts/:accountUid` | [docs](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k) |
| [Update Deal](actions/update-deal.md) | `PUT /crm/deals/:dealUid` | [docs](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k) |
| [Update Person](actions/update-person.md) | `PUT /crm/people/:personUid` | [docs](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k) |
| [Update Person Account Membership](actions/update-person-account-membership.md) | `PUT /crm/accounts/:accountUid/memberships/:membershipUid` | [docs](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k) |
