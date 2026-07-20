# <img src="https://images.mindcloud.co/apps/icons/dripcel_1774994899530.png" alt="Dripcel logo" width="28" height="28"> Dripcel: Universal API

Dripcel through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dripcel/latest
- **Category:** Marketing
- **Actions:** 28
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://dripcel.com
- **Vendor API docs:** https://docs.dripcel.com/API/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Credit Balance](actions/get-credit-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dripcel/latest/actions/get-credit-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (28)

### Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Credit Balance](actions/get-credit-balance.md) | GET | Retrieves the credit balance from Dripcel. |

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a campaign from Dripcel by ID. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns from Dripcel. |

### Compliance Check

| Action | Method | Description |
| --- | --- | --- |
| [Check Cell Numbers](actions/check-cell-numbers.md) | POST | Checks whether cell numbers can receive a Dripcel campaign. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Add Tags to Contact](actions/add-tags-to-contact.md) | PUT | Updates a contact to add tags in Dripcel. |
| [Bulk Update Contacts](actions/bulk-update-contacts.md) | PUT | Updates contacts in Dripcel in bulk. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes a contact from Dripcel by cell number. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Dripcel by cell number. |
| [Opt Out Contact](actions/opt-out-contact.md) | PUT | Updates a contact to opt out of multiple Dripcel campaigns. |
| [Opt Out Contact from Campaign](actions/opt-out-contact-from-campaign.md) | PUT | Updates a contact to opt out of one Dripcel campaign. |
| [Remove Tags from Contact](actions/remove-tags-from-contact.md) | PUT | Updates a contact to remove tags in Dripcel. |
| [Search Contacts](actions/search-contacts.md) | GET | Finds contacts in Dripcel. |
| [Update Contacts](actions/update-contacts.md) | PUT | Updates contacts in Dripcel, creating missing contacts when needed. |
| [Upload Contacts](actions/upload-contacts.md) | POST | Creates new contacts in Dripcel. |

### Delivery

| Action | Method | Description |
| --- | --- | --- |
| [List Deliveries](actions/list-deliveries.md) | GET | Retrieves deliveries from Dripcel. |

### Reply

| Action | Method | Description |
| --- | --- | --- |
| [Search Replies](actions/search-replies.md) | GET | Finds replies in Dripcel. |

### Sale

| Action | Method | Description |
| --- | --- | --- |
| [Upload Sale](actions/upload-sale.md) | POST | Creates a sale in Dripcel. |
| [Upload Sales](actions/upload-sales.md) | POST | Creates sales in Dripcel in bulk. |

### Send

| Action | Method | Description |
| --- | --- | --- |
| [Send Bulk Email](actions/send-bulk-email.md) | POST | Creates a bulk email send in Dripcel. |
| [Send SMS](actions/send-sms.md) | POST | Creates a single SMS send in Dripcel. |

### Send Log

| Action | Method | Description |
| --- | --- | --- |
| [Get Send Log](actions/get-send-log.md) | GET | Retrieves a send log from Dripcel by ID. |
| [Search Send Logs](actions/search-send-logs.md) | GET | Finds send logs in Dripcel. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Delete Tag](actions/delete-tag.md) | DELETE | Deletes a tag from Dripcel by ID. |
| [Get Tag](actions/get-tag.md) | GET | Retrieves a tag from Dripcel by ID. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from Dripcel. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [List Email Templates](actions/list-email-templates.md) | GET | Retrieves email templates from Dripcel. |

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [Search Transactions](actions/search-transactions.md) | GET | Finds buyer transactions in Dripcel Exchange. |
| [Update Transaction Status](actions/update-transaction-status.md) | PUT | Updates a buyer transaction status in Dripcel Exchange. |

