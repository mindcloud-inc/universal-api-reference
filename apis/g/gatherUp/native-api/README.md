# GatherUp: Native API Reference

A consolidated summary of GatherUp's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://app.gatherup.com/api/doc
- **API base URL:** `https://app.gatherup.com/api`

## Authentication

### Bearer Token

Use a GatherUp bearer token and client ID to authorize API requests.

### Credentials

- **API Key:** `apiKey` · required
- **Client ID:** `clientId` · required · GatherUp client ID required on every API request.
- **Agent ID:** `agent` · optional · Optional GatherUp agency client identifier used with global API credentials.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://app.gatherup.com/api/doc/bearer)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The total page count is read from `pages`. The current page number is read from `page`.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Email to Receive Notifications](actions/add-email-to-receive-notifications.md) | `POST /business/notifications/email/add` | [docs](https://app.gatherup.com/api/doc/business/notifications/email/add) |
| [Add Online Review Link](actions/add-online-review-link.md) | `POST /business/online-review-link/add` | [docs](https://app.gatherup.com/api/doc/business/online-review-link/add) |
| [Auto Feedback Requests](actions/auto-feedback-requests.md) | `POST /business/auto-feedback-requests` | [docs](https://app.gatherup.com/api/doc/business/auto-feedback-requests) |
| [Create Business](actions/create-business.md) | `POST /business/create` | [docs](https://app.gatherup.com/api/doc/business/create) |
| [Create Customer](actions/create-customer.md) | `POST /customer/create` | [docs](https://app.gatherup.com/api/doc/customer/create) |
| [Create Multiple Customers](actions/create-multiple-customers.md) | `POST /customers/create` | [docs](https://app.gatherup.com/api/doc/customers/create) |
| [Create User](actions/create-user.md) | `POST /user/create` | [docs](https://app.gatherup.com/api/doc/user/create) |
| [Deactivate Business](actions/deactivate-business.md) | `POST /business/deactivate` | [docs](https://app.gatherup.com/api/doc/business/deactivate) |
| [Deactivate User](actions/deactivate-user.md) | `POST /user/deactivate` | [docs](https://app.gatherup.com/api/doc/user/deactivate) |
| [Delete Business](actions/delete-business.md) | `POST /business/delete` | [docs](https://app.gatherup.com/api/doc/business/delete) |
| [Delete Customer](actions/delete-customer.md) | `POST /customer/delete` | [docs](https://app.gatherup.com/api/doc/customer/delete) |
| [Get Business](actions/get-business.md) | `POST /business/get` | [docs](https://app.gatherup.com/api/doc/business/get) |
| [Get Business Survey Results](actions/get-business-survey-results.md) | `POST /survey-questions/average/get` | [docs](https://app.gatherup.com/api/doc/survey-questions/average/get) |
| [Get Customer](actions/get-customer.md) | `POST /customer/get` | [docs](https://app.gatherup.com/api/doc/customer/get) |
| [Get Customer Survey Answers](actions/get-customer-survey-answers.md) | `POST /survey-questions/customer/get` | [docs](https://app.gatherup.com/api/doc/survey-questions/customer/get) |
| [Get Feedbacks Received](actions/get-feedbacks-received.md) | `POST /feedbacks/get` | [docs](https://app.gatherup.com/api/doc/feedbacks/get) |
| [List Business Types](actions/list-business-types.md) | `POST /business/types` | [docs](https://app.gatherup.com/api/doc/business/types) |
| [List Businesses](actions/list-businesses.md) | `POST /businesses/get` | [docs](https://app.gatherup.com/api/doc/businesses/get) |
| [List Customers](actions/list-customers.md) | `POST /customers/get` | [docs](https://app.gatherup.com/api/doc/customers/get) |
| [List Facebook Recommendations](actions/list-facebook-recommendations.md) | `POST /facebook-recommendations/get` | [docs](https://app.gatherup.com/api/doc/facebook-recommendations/get) |
| [List Feedback Responses](actions/list-feedback-responses.md) | `POST /feedbacks/responses/get` | [docs](https://app.gatherup.com/api/doc/feedbacks/responses/get) |
| [List Google Q&A](actions/list-google-qa.md) | `GET /google-qa/get` | [docs](https://app.gatherup.com/api/doc/google-qa/get) |
| [List Online Review Links](actions/list-online-review-links.md) | `POST /business/online-review-links/get` | [docs](https://app.gatherup.com/api/doc/business/online-review-links/get) |
| [List Online Reviews Received](actions/list-online-reviews-received.md) | `POST /online-reviews/get` | [docs](https://app.gatherup.com/api/doc/online-reviews/get) |
| [List Show-Hide History](actions/list-show-hide-history.md) | `POST /feedbacks/show-hide-history` | [docs](https://app.gatherup.com/api/doc/feedbacks/show-hide-history) |
| [List Users](actions/list-users.md) | `POST /user/managers/get` | [docs](https://app.gatherup.com/api/doc/user/managers/get) |
| [Reactivate Business](actions/reactivate-business.md) | `POST /business/reactivate` | [docs](https://app.gatherup.com/api/doc/business/reactivate) |
| [Reactivate User](actions/reactivate-user.md) | `POST /user/reactivate` | [docs](https://app.gatherup.com/api/doc/user/reactivate) |
| [Remove Email from Notifications](actions/remove-email-from-notifications.md) | `POST /business/notifications/email/remove` | [docs](https://app.gatherup.com/api/doc/business/notifications/email/remove) |
| [Reply to Customer](actions/reply-to-customer.md) | `POST /customer/reply` | [docs](https://app.gatherup.com/api/doc/customer/reply) |
| [Reply to Online Review](actions/reply-to-online-review.md) | `POST /online-review/reply` | [docs](https://app.gatherup.com/api/doc/online-review/reply) |
| [Search for Business ID](actions/search-for-business-id.md) | `POST /business/search` | [docs](https://app.gatherup.com/api/doc/business/search) |
| [Send Customer Feedback Request](actions/send-customer-feedback-request.md) | `POST /customer/feedback/send` | [docs](https://app.gatherup.com/api/doc/customer/feedback/send) |
| [Set User Password](actions/set-user-password.md) | `POST /user/password/set` | [docs](https://app.gatherup.com/api/doc/user/password/set) |
| [Update Business](actions/update-business.md) | `POST /business/update` | [docs](https://app.gatherup.com/api/doc/business/update) |
| [Update Customer](actions/update-customer.md) | `POST /customer/update` | [docs](https://app.gatherup.com/api/doc/customer/update) |
| [Update Customer Feedback](actions/update-customer-feedback.md) | `POST /customer/feedback/update` | [docs](https://app.gatherup.com/api/doc/customer/feedback/update) |
| [Update Online Review Link URL](actions/update-online-review-link-url.md) | `POST /business/online-review-link/update` | [docs](https://app.gatherup.com/api/doc/business/online-review-link/update) |
| [Update User Information](actions/update-user-information.md) | `POST /user/manager/update` | [docs](https://app.gatherup.com/api/doc/user/manager/update) |
| [Update User Managed Businesses](actions/update-user-managed-businesses.md) | `POST /user/update-managed-businesses` | [docs](https://app.gatherup.com/api/doc/user/update-managed-businesses) |
