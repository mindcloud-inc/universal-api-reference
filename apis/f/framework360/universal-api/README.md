# <img src="https://images.mindcloud.co/apps/icons/framework360_1775826508289.png" alt="Framework360 logo" width="28" height="28"> Framework360: Universal API

Manage customers, orders, content, and campaigns in Framework360

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/framework360/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 86
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://mindcloudstage0.framework360.site/
- **Vendor API docs:** https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Profile](actions/get-user-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/framework360/latest/actions/get-user-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (86)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Login User](actions/login-user.md) | POST |  |

### Applications

| Action | Method | Description |
| --- | --- | --- |
| [Install Plugin](actions/plugins-install.md) | POST |  |
| [Get Plugin Settings](actions/plugins-settings.md) | GET |  |

### Attachments

| Action | Method | Description |
| --- | --- | --- |
| [Add Media](actions/media-add.md) | POST |  |
| [Delete Media](actions/media-delete.md) | DELETE |  |
| [List Media](actions/media-directories.md) | GET |  |
| [Format Media](actions/media-format.md) | PUT |  |
| [List Media](actions/media-list.md) | GET |  |
| [Update Media](actions/media-update.md) | PUT |  |

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [List Campaign Action Stats](actions/marketing-campaigns-action-stats.md) | GET |  |
| [Get Campaign Action Summary](actions/marketing-campaigns-action-summary.md) | GET |  |
| [List Campaign Contacts](actions/marketing-campaigns-contacts.md) | GET |  |
| [Get Campaign Flow](actions/marketing-campaigns-flow.md) | GET |  |
| [List Campaign Statuses](actions/marketing-campaigns-statuses.md) | GET |  |
| [List Campaign Types](actions/marketing-campaigns-types.md) | GET |  |
| [Update Campaign Status](actions/marketing-campaigns-updatestatus.md) | PUT |  |

### Checkouts

| Action | Method | Description |
| --- | --- | --- |
| [Get Checkout](actions/checkouts-get.md) | GET |  |

### Connections

| Action | Method | Description |
| --- | --- | --- |
| [Check Connection](actions/check-connection.md) | GET |  |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Delete Customer](actions/customers-delete.md) | DELETE |  |
| [Get Customer](actions/customers-get.md) | GET |  |
| [Create Customer History](actions/customers-history-create.md) | POST |  |
| [List Customer History](actions/customers-history-list.md) | GET |  |
| [Update Customer History](actions/customers-history-update.md) | PUT |  |
| [List Customer](actions/customers-list.md) | GET |  |
| [Login Customer](actions/customers-login.md) | POST |  |
| [List Customer Notification](actions/customers-notifications-list.md) | GET |  |
| [Mark Customer Notification](actions/customers-notifications-mark.md) | PUT |  |
| [Register Customer Notification](actions/customers-notifications-register.md) | POST |  |
| [Get Customer Notification](actions/customers-notifications-status.md) | GET |  |
| [Unregister Customer Notification](actions/customers-notifications-unregister.md) | PUT |  |
| [Get Customer Profile](actions/customers-profile.md) | GET |  |
| [Register Customer](actions/customers-registration.md) | POST |  |
| [Search Customer](actions/customers-search.md) | GET |  |
| [List Customer Sources](actions/customers-sources.md) | GET |  |
| [Update Customer](actions/customers-update.md) | PUT |  |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [List Payments](actions/payments-list.md) | GET |  |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [List Report Categories](actions/reports-categories.md) | GET |  |
| [Get Report](actions/reports-get.md) | GET |  |

### Sales Orders

| Action | Method | Description |
| --- | --- | --- |
| [Apply Order](actions/orders-applycoupon.md) | POST |  |
| [Cancel Order](actions/orders-cancel.md) | DELETE |  |
| [List Order Coupons](actions/orders-coupons.md) | GET |  |
| [Create Order](actions/orders-create.md) | POST |  |
| [Delete Order](actions/orders-delete.md) | DELETE |  |
| [Get Order](actions/orders-get.md) | GET |  |
| [List Order Labels](actions/orders-labels.md) | GET |  |
| [List Order](actions/orders-list.md) | GET |  |
| [Prepare Order](actions/orders-preparecart.md) | POST |  |
| [Repeat Order](actions/orders-repeat.md) | POST |  |
| [Resend Order](actions/orders-resendnotifications.md) | PUT |  |
| [Calculate Order](actions/orders-shippings.md) | PUT |  |
| [List Order Statuses](actions/orders-statuses.md) | GET |  |
| [Update Order](actions/orders-updatestatus.md) | PUT |  |

### Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [Add Subscription](actions/subscriptions-addsubscription.md) | POST |  |
| [Get Subscription Status](actions/subscriptions-getsubscriptionstatus.md) | GET |  |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [List Marketing Tags](actions/marketing-tags.md) | GET |  |

### Tax Rates

| Action | Method | Description |
| --- | --- | --- |
| [List Payment Taxes](actions/payments-taxes.md) | GET |  |

### Threads

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat](actions/chat-create.md) | POST |  |
| [Get Chat](actions/chat-get.md) | GET |  |
| [List Chat](actions/chat-list.md) | GET |  |
| [Mark Chat](actions/chat-markas.md) | PUT |  |
| [List Chat Messages](actions/chat-messages.md) | GET |  |
| [Reply Chat](actions/chat-reply.md) | PUT |  |
| [List Chat Types](actions/chat-types.md) | GET |  |
| [Update Chat](actions/chat-updatestatus.md) | PUT |  |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Content Slider](actions/content-sliders-get.md) | GET |  |
| [Get Dashboard](actions/dashboard-get.md) | GET |  |
| [Get Datatable](actions/datatables-get.md) | GET |  |
| [Submit Form](actions/forms-submit.md) | POST |  |
| [List Search](actions/search-list.md) | GET |  |
| [List Site Assets](actions/site-assets.md) | GET |  |
| [Get Site Data](actions/site-data.md) | GET |  |
| [List Site Plugins](actions/site-plugins.md) | GET |  |
| [Get Site Settings](actions/site-settings.md) | GET |  |
| [Get Site Theme](actions/site-theme.md) | GET |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User Profile](actions/get-user-profile.md) | GET |  |
| [Delete User](actions/users-delete.md) | DELETE |  |
| [Get User](actions/users-get.md) | GET |  |
| [List User](actions/users-list.md) | GET |  |
| [Register User Notification](actions/users-notifications-register.md) | POST |  |
| [Unregister User Notification](actions/users-notifications-unregister.md) | PUT |  |
| [Register User](actions/users-registration.md) | POST |  |
| [Reset User](actions/users-reset.md) | PUT |  |
| [Update User](actions/users-update.md) | PUT |  |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/webhooks-create.md) | POST |  |
| [Delete Webhook](actions/webhooks-delete.md) | DELETE |  |
| [Test Webhook](actions/webhooks-test.md) | PUT |  |

