# <img src="https://images.mindcloud.co/apps/icons/peach_1774900064843.png" alt="Peach logo" width="28" height="28"> Peach: Universal API

Peach is a fundraising and nonprofit management platform for campaigns, contacts, payments, transactions, and notes.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/peach/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.peach-in.com
- **Vendor API docs:** https://peach-organization.gitbook.io/peach/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Transactions](actions/list-transactions.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/peach/latest/actions/list-transactions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a campaign from Peach. |

### Campaign Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign Stats](actions/get-campaign-stats.md) | GET | Retrieves campaign performance statistics from Peach. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Peach. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Peach. |
| [Get Contact By Email](actions/get-contact-by-email.md) | GET | Retrieves a contact from Peach by email address. |
| [Get Contact By ID](actions/get-contact-by-id.md) | GET | Retrieves a contact from Peach by ID. |
| [Get Contact By Phone](actions/get-contact-by-phone.md) | GET | Retrieves a contact from Peach by phone number. |
| [Get Contact By Tz](actions/get-contact-by-tz.md) | GET | Retrieves a contact from Peach by tz identifier. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Peach. |

### Note

| Action | Method | Description |
| --- | --- | --- |
| [Create Note](actions/create-note.md) | POST | Creates a note for a contact in Peach. |

### Payment

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Subscription](actions/cancel-subscription.md) | PUT | Updates a subscription payment in Peach by canceling it. |
| [Change Subscription Charge Day](actions/change-subscription-charge-day.md) | PUT | Updates a subscription payment in Peach with a new charge day. |
| [Create One-Time Payment](actions/create-one-time-payment.md) | POST | Creates a one-time payment in Peach. |
| [Create Subscription Payment](actions/create-subscription-payment.md) | POST | Creates a subscription payment in Peach. |
| [Freeze Subscription](actions/freeze-subscription.md) | PUT | Updates a subscription payment in Peach by freezing it. |
| [Update Payment Field](actions/update-payment-field.md) | PUT | Updates a payment field in Peach. |
| [Update Subscription Additional Sum](actions/update-subscription-additional-sum.md) | PUT | Updates a subscription payment in Peach with a new recurring sum. |
| [Update Subscription Cycles](actions/update-subscription-cycles.md) | PUT | Updates a subscription payment in Peach with new billing cycles. |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [List Transactions](actions/list-transactions.md) | GET | Retrieves transaction records from Peach. |
| [List Transactions By Campaign](actions/list-transactions-by-campaign.md) | GET | Retrieves transaction records from Peach by campaign ID. |

