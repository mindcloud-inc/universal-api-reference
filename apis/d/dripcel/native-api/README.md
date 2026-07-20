# Dripcel: Native API Reference

A consolidated summary of Dripcel's API configuration and 28 documented operations, with links to official documentation.

- **Official docs:** https://docs.dripcel.com/API/overview
- **API base URL:** `https://api.dripcel.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.dripcel.com/API/overview)

## Endpoints (28 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Tags to Contact](actions/add-tags-to-contact.md) | `PUT /contacts/:cell/tag/add` | [docs](https://docs.dripcel.com/API/contacts#add-or-remove-tags-from-a-contact) |
| [Bulk Update Contacts](actions/bulk-update-contacts.md) | `POST /contacts/update` | [docs](https://docs.dripcel.com/API/contacts#bulk-update-contacts) |
| [Check Cell Numbers](actions/check-cell-numbers.md) | `POST /compliance/send` | [docs](https://docs.dripcel.com/API/compliance#check-a-list-of-cell-numbers) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/:cell` | [docs](https://docs.dripcel.com/API/contacts#delete-a-single-contact) |
| [Delete Tag](actions/delete-tag.md) | `DELETE /tags/:tag_id` | [docs](https://docs.dripcel.com/API/tags#delete-a-single-tag) |
| [Get Campaign](actions/get-campaign.md) | `GET /campaigns/:campaign_id` | [docs](https://docs.dripcel.com/API/campaigns#view-a-single-campaign) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:cell` | [docs](https://docs.dripcel.com/API/contacts#get-a-single-contact) |
| [Get Credit Balance](actions/get-credit-balance.md) | `GET /balance` | [docs](https://docs.dripcel.com/API/balance) |
| [Get Send Log](actions/get-send-log.md) | `GET /send-logs/:send_id` | [docs](https://docs.dripcel.com/API/send-logs#view-a-single-send-log) |
| [Get Tag](actions/get-tag.md) | `GET /tags/:tag_id` | [docs](https://docs.dripcel.com/API/tags#view-a-single-tag) |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaigns` | [docs](https://docs.dripcel.com/API/campaigns#view-all-campaigns) |
| [List Deliveries](actions/list-deliveries.md) | `GET /deliveries` | [docs](https://docs.dripcel.com/API/deliveries) |
| [List Email Templates](actions/list-email-templates.md) | `GET /email/templates` | [docs](https://docs.dripcel.com/API/email-templates) |
| [List Tags](actions/list-tags.md) | `GET /tags` | [docs](https://docs.dripcel.com/API/tags#view-all-tags) |
| [Opt Out Contact](actions/opt-out-contact.md) | `POST /contacts/:cell/optOut` | [docs](https://docs.dripcel.com/API/contacts#opt-out-a-contact) |
| [Opt Out Contact from Campaign](actions/opt-out-contact-from-campaign.md) | `PUT /contacts/:cell/optOut` | [docs](https://docs.dripcel.com/API/contacts#opt-out-a-contact) |
| [Remove Tags from Contact](actions/remove-tags-from-contact.md) | `PUT /contacts/:cell/tag/remove` | [docs](https://docs.dripcel.com/API/contacts#add-or-remove-tags-from-a-contact) |
| [Search Contacts](actions/search-contacts.md) | `POST /contacts/search` | [docs](https://docs.dripcel.com/API/contacts#search-for-contacts) |
| [Search Replies](actions/search-replies.md) | `POST /replies/search` | [docs](https://docs.dripcel.com/API/replies#search-replies) |
| [Search Send Logs](actions/search-send-logs.md) | `POST /send-logs/search` | [docs](https://docs.dripcel.com/API/send-logs#search-send-logs) |
| [Search Transactions](actions/search-transactions.md) | `POST /exchange/buyer/transaction/search` | [docs](https://docs.dripcel.com/API/exchange-transactions#search-transactions) |
| [Send Bulk Email](actions/send-bulk-email.md) | `POST /send/email/bulk` | [docs](https://docs.dripcel.com/API/send#send-bulk-email) |
| [Send SMS](actions/send-sms.md) | `POST /send/sms` | [docs](https://docs.dripcel.com/API/send#send-a-single-sms) |
| [Update Contacts](actions/update-contacts.md) | `PUT /contacts` | [docs](https://docs.dripcel.com/API/contacts#upload-contacts) |
| [Update Transaction Status](actions/update-transaction-status.md) | `PUT /exchange/buyer/transaction/:id/status` | [docs](https://docs.dripcel.com/API/exchange-transactions#update-transaction-status) |
| [Upload Contacts](actions/upload-contacts.md) | `POST /contacts` | [docs](https://docs.dripcel.com/API/contacts#upload-contacts) |
| [Upload Sale](actions/upload-sale.md) | `GET /sales/create` | [docs](https://docs.dripcel.com/API/sales#get-request) |
| [Upload Sales](actions/upload-sales.md) | `POST /sales` | [docs](https://docs.dripcel.com/API/sales#post-request) |
