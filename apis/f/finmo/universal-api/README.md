# <img src="https://images.mindcloud.co/apps/icons/images-2_1773623957293.jpeg" alt="Finmo logo" width="28" height="28"> Finmo: Universal API

Manage wallets, customers, payins, payouts, and refunds

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/finmo/latest
- **Category:** Commerce / Accounting
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.finmo.net
- **Vendor API docs:** https://docs.finmo.net/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Wallets](actions/list-wallets.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finmo/latest/actions/list-wallets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in Finmo. |
| [Disable Customer](actions/disable-customer.md) | PUT | Disables an existing customer in Finmo. |
| [Enable Customer](actions/enable-customer.md) | PUT | Enables an existing customer in Finmo. |
| [Get Customer](actions/get-customer.md) | GET | Finds a customer in Finmo by ID. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from the Finmo platform. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in Finmo. |

### Payin

| Action | Method | Description |
| --- | --- | --- |
| [Create Payin](actions/create-payin.md) | POST | Creates a new payin in Finmo. |
| [List Payins](actions/list-payins.md) | GET | Retrieves payins from the Finmo platform. |
| [Retrieve Payin](actions/retrieve-payin.md) | GET | Finds a payin in Finmo by ID. |

### Payout

| Action | Method | Description |
| --- | --- | --- |
| [Create Payout](actions/create-payout.md) | POST | Creates a new payout in Finmo. |
| [List Payouts](actions/list-payouts.md) | GET | Retrieves payouts from the Finmo platform. |
| [Retrieve Payout](actions/retrieve-payout.md) | GET | Finds a payout in Finmo by ID. |

### Payout Beneficiary

| Action | Method | Description |
| --- | --- | --- |
| [Create Payout Beneficiary](actions/create-payout-beneficiary.md) | POST | Creates a new payout beneficiary in Finmo. |
| [List Payout Beneficiaries](actions/list-payout-beneficiaries.md) | GET | Retrieves payout beneficiaries from the Finmo platform. |

### Payout Sender

| Action | Method | Description |
| --- | --- | --- |
| [Create Payout Sender](actions/create-payout-sender.md) | POST | Creates a new payout sender in Finmo. |
| [List Payout Senders](actions/list-payout-senders.md) | GET | Retrieves payout senders from the Finmo platform. |

### Refund

| Action | Method | Description |
| --- | --- | --- |
| [Create Refund](actions/create-refund.md) | POST | Creates a new refund in Finmo. |
| [List Refunds](actions/list-refunds.md) | GET | Retrieves refunds from the Finmo platform. |
| [Retrieve Refund](actions/retrieve-refund.md) | GET | Finds a refund in Finmo by ID. |

### Virtual Account

| Action | Method | Description |
| --- | --- | --- |
| [Create Virtual Account](actions/create-virtual-account.md) | POST | Creates a new virtual account in Finmo. |
| [Delete Virtual Account](actions/delete-virtual-account.md) | DELETE | Deletes an existing virtual account from Finmo. |
| [Get Virtual Account](actions/get-virtual-account.md) | GET | Finds a virtual account in Finmo by ID. |
| [List Virtual Accounts](actions/list-virtual-accounts.md) | GET | Retrieves virtual accounts from the Finmo platform. |

### Wallet

| Action | Method | Description |
| --- | --- | --- |
| [List Wallets](actions/list-wallets.md) | GET | Retrieves wallets from the Finmo platform. |

