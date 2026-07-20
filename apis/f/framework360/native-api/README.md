# Framework360: Native API Reference

A consolidated summary of Framework360's API configuration and 86 documented operations, with links to official documentation.

- **Official docs:** https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/
- **API base URL:** `https://mindcloudstage0.framework360.site/m/api`

## Authentication

### Framework360 API Key

Connect with a Framework360 API key, with optional user token for user-authenticated calls.

### Credentials

- **API Key:** `apiKey` · required · Framework360 API key sent as X-Fw360-Key.
- **User Token:** `userToken` · optional · Optional Framework360 user access token sent as X-Fw360-UserToken for user-authenticated API calls.
- **User Email:** `email` · optional · Framework360 backoffice email used to obtain a user token through /m/api/users/login when needed.

[Official authentication documentation](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Endpoints (86 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Chat](actions/chat-create.md) | `POST chat/create` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Get Chat](actions/chat-get.md) | `GET chat/get` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [List Chat](actions/chat-list.md) | `GET chat/list` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Mark Chat](actions/chat-markas.md) | `POST chat/markAs` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [List Chat Messages](actions/chat-messages.md) | `GET chat/messages` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Reply Chat](actions/chat-reply.md) | `POST chat/reply` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [List Chat Types](actions/chat-types.md) | `GET chat/types` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Update Chat](actions/chat-updatestatus.md) | `POST chat/updateStatus` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Check Connection](actions/check-connection.md) | `GET check` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Get Checkout](actions/checkouts-get.md) | `GET checkouts/get` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Get Content Slider](actions/content-sliders-get.md) | `GET content/sliders/get` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Delete Customer](actions/customers-delete.md) | `POST customers/delete` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Get Customer](actions/customers-get.md) | `GET customers/get` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Create Customer History](actions/customers-history-create.md) | `POST customers/history/create` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [List Customer History](actions/customers-history-list.md) | `GET customers/history/list` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Update Customer History](actions/customers-history-update.md) | `POST customers/history/update` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [List Customer](actions/customers-list.md) | `GET customers/list` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Login Customer](actions/customers-login.md) | `POST customers/login` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [List Customer Notification](actions/customers-notifications-list.md) | `GET customers/notifications/list` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Mark Customer Notification](actions/customers-notifications-mark.md) | `POST customers/notifications/mark` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Register Customer Notification](actions/customers-notifications-register.md) | `POST customers/notifications/register` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Get Customer Notification](actions/customers-notifications-status.md) | `GET customers/notifications/status` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Unregister Customer Notification](actions/customers-notifications-unregister.md) | `POST customers/notifications/unregister` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Get Customer Profile](actions/customers-profile.md) | `GET customers/profile` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Register Customer](actions/customers-registration.md) | `POST customers/registration` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Search Customer](actions/customers-search.md) | `GET customers/search` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [List Customer Sources](actions/customers-sources.md) | `GET customers/sources` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Update Customer](actions/customers-update.md) | `POST customers/update` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Get Dashboard](actions/dashboard-get.md) | `GET dashboard/get` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Get Datatable](actions/datatables-get.md) | `GET datatables/get` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Submit Form](actions/forms-submit.md) | `POST forms/submit` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Get User Profile](actions/get-user-profile.md) | `GET users/profile` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Login User](actions/login-user.md) | `POST users/login` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [List Campaign Action Stats](actions/marketing-campaigns-action-stats.md) | `GET marketing/campaigns/action/stats` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Get Campaign Action Summary](actions/marketing-campaigns-action-summary.md) | `GET marketing/campaigns/action/summary` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [List Campaign Contacts](actions/marketing-campaigns-contacts.md) | `GET marketing/campaigns/contacts` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Get Campaign Flow](actions/marketing-campaigns-flow.md) | `GET marketing/campaigns/flow` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [List Campaign Statuses](actions/marketing-campaigns-statuses.md) | `GET marketing/campaigns/statuses` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [List Campaign Types](actions/marketing-campaigns-types.md) | `GET marketing/campaigns/types` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Update Campaign Status](actions/marketing-campaigns-updatestatus.md) | `POST marketing/campaigns/updateStatus` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [List Marketing Tags](actions/marketing-tags.md) | `GET marketing/tags` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Add Media](actions/media-add.md) | `POST media/add` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Delete Media](actions/media-delete.md) | `POST media/delete` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [List Media](actions/media-directories.md) | `GET media/directories` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Format Media](actions/media-format.md) | `POST media/format` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [List Media](actions/media-list.md) | `GET media/list` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Update Media](actions/media-update.md) | `POST media/update` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Apply Order](actions/orders-applycoupon.md) | `POST orders/applyCoupon` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Cancel Order](actions/orders-cancel.md) | `POST orders/cancel` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [List Order Coupons](actions/orders-coupons.md) | `GET orders/coupons` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Create Order](actions/orders-create.md) | `POST orders/create` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Delete Order](actions/orders-delete.md) | `POST orders/delete` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Get Order](actions/orders-get.md) | `GET orders/get` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [List Order Labels](actions/orders-labels.md) | `GET orders/labels` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [List Order](actions/orders-list.md) | `GET orders/list` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Prepare Order](actions/orders-preparecart.md) | `POST orders/prepareCart` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Repeat Order](actions/orders-repeat.md) | `POST orders/repeat` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Resend Order](actions/orders-resendnotifications.md) | `POST orders/resendNotifications` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Calculate Order](actions/orders-shippings.md) | `POST orders/shippings` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [List Order Statuses](actions/orders-statuses.md) | `GET orders/statuses` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Update Order](actions/orders-updatestatus.md) | `POST orders/updateStatus` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [List Payments](actions/payments-list.md) | `GET payments/list` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [List Payment Taxes](actions/payments-taxes.md) | `GET payments/taxes` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Install Plugin](actions/plugins-install.md) | `POST plugins/install` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Get Plugin Settings](actions/plugins-settings.md) | `GET plugins/settings` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [List Report Categories](actions/reports-categories.md) | `GET reports/categories` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Get Report](actions/reports-get.md) | `POST reports/get` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [List Search](actions/search-list.md) | `GET search/list` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [List Site Assets](actions/site-assets.md) | `GET site/assets` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Get Site Data](actions/site-data.md) | `GET site/data` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [List Site Plugins](actions/site-plugins.md) | `GET site/plugins` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Get Site Settings](actions/site-settings.md) | `GET site/settings` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Get Site Theme](actions/site-theme.md) | `GET site/theme` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Add Subscription](actions/subscriptions-addsubscription.md) | `POST subscriptions/addSubscription` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Get Subscription Status](actions/subscriptions-getsubscriptionstatus.md) | `GET subscriptions/getSubscriptionStatus` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Delete User](actions/users-delete.md) | `POST users/delete` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Get User](actions/users-get.md) | `GET users/get` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [List User](actions/users-list.md) | `GET users/list` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Register User Notification](actions/users-notifications-register.md) | `POST users/notifications/register` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Unregister User Notification](actions/users-notifications-unregister.md) | `POST users/notifications/unregister` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Register User](actions/users-registration.md) | `POST users/registration` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Reset User](actions/users-reset.md) | `POST users/reset` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Update User](actions/users-update.md) | `POST users/update` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Create Webhook](actions/webhooks-create.md) | `POST webhooks/create` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Delete Webhook](actions/webhooks-delete.md) | `POST webhooks/delete` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
| [Test Webhook](actions/webhooks-test.md) | `GET webhooks/test` | [docs](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/) |
