# <img src="https://images.mindcloud.co/apps/icons/instant-card_1774899862041.png" alt="InstantCard logo" width="28" height="28"> InstantCard: Universal API

Create, print, and manage ID cards and templates

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/instantCard/latest
- **Actions:** 37
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://instantcard.net/
- **Vendor API docs:** https://instantcard.net/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get My Profile](actions/get-my-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/get-my-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (37)

### Add Funds

| Action | Method | Description |
| --- | --- | --- |
| [Add Funds](actions/add-funds.md) | POST | Adds funds to an InstantCard organization balance. |

### Address

| Action | Method | Description |
| --- | --- | --- |
| [Create Address](actions/create-address.md) | POST | Creates a new address in InstantCard. |
| [Delete Address](actions/delete-address.md) | DELETE | Deletes an existing address from InstantCard. |
| [Get Address](actions/get-address.md) | GET | Retrieves an address from InstantCard by ID. |
| [List Addresses](actions/list-addresses.md) | GET | Retrieves all saved addresses from InstantCard. |
| [Update Address](actions/update-address.md) | PUT | Updates an existing address in InstantCard. |

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Delete Card](actions/delete-card.md) | DELETE | Deletes an existing card from InstantCard. |

### Card

| Action | Method | Description |
| --- | --- | --- |
| [Create Card](actions/create-card.md) | POST | Creates a new draft card in InstantCard. |
| [Finalize Card](actions/finalize-card.md) | PUT | Updates an existing card in InstantCard by finalizing it. |
| [Get Card](actions/get-card.md) | GET | Retrieves a card from InstantCard by ID. |
| [List Cards](actions/list-cards.md) | GET | Retrieves all organization cards from InstantCard. |
| [Search Cards](actions/search-cards.md) | GET | Finds cards in InstantCard by search terms. |
| [Update Card](actions/update-card.md) | PUT | Updates an existing card in InstantCard. |

### Card Preview

| Action | Method | Description |
| --- | --- | --- |
| [Preview Card](actions/preview-card.md) | GET | Retrieves a card preview from InstantCard. |

### Card Print History

| Action | Method | Description |
| --- | --- | --- |
| [List Card Print History](actions/list-card-print-history.md) | GET | Retrieves print history for a card in InstantCard. |

### Card Template

| Action | Method | Description |
| --- | --- | --- |
| [List Card Templates](actions/list-card-templates.md) | GET | Retrieves available card templates from InstantCard. |

### Card Template Field

| Action | Method | Description |
| --- | --- | --- |
| [Get Card Template Fields](actions/get-card-template-fields.md) | GET | Retrieves card template fields from InstantCard. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in InstantCard. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from InstantCard. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from InstantCard by ID. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves all organization contacts from InstantCard. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in InstantCard. |

### Financial Transaction

| Action | Method | Description |
| --- | --- | --- |
| [List Financial Transactions](actions/list-financial-transactions.md) | GET | Retrieves all financial transactions from InstantCard. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Check Print Job Balance](actions/check-print-job-balance.md) | GET | Retrieves whether an InstantCard print job is covered by available funds. |
| [Get Print Job](actions/get-print-job.md) | GET | Retrieves a print job from InstantCard by ID. |
| [Get Print Job Charge Details](actions/get-print-job-charge-details.md) | GET | Retrieves submitted print job charge details from InstantCard. |
| [List Print Jobs](actions/list-print-jobs.md) | GET | Retrieves a list of print jobs from InstantCard. |
| [Remove Card From Print Job](actions/remove-card-from-print-job.md) | PUT | Updates an existing print job in InstantCard by removing a card. |
| [Submit Print Job](actions/submit-print-job.md) | PUT | Updates an existing print job in InstantCard by submitting it. |
| [Update Print Job](actions/update-print-job.md) | PUT | Updates an existing print job in InstantCard. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET | Retrieves an organization from InstantCard by ID. |

### Organization Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization Balance](actions/get-organization-balance.md) | GET | Retrieves an organization's current balance from InstantCard. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Authenticate User](actions/authenticate-user.md) | GET | Retrieves an authentication token from InstantCard by user credentials. |

### Print Job

| Action | Method | Description |
| --- | --- | --- |
| [Add Cards To Print Job](actions/add-cards-to-print-job.md) | PUT | Updates an existing print job in InstantCard by adding cards. |
| [Create Print Job](actions/create-print-job.md) | POST | Creates a new print job in InstantCard. |

### Shipping Provider

| Action | Method | Description |
| --- | --- | --- |
| [List Shipping Providers](actions/list-shipping-providers.md) | GET | Retrieves available shipping providers from InstantCard. |

### User Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get My Profile](actions/get-my-profile.md) | GET | Retrieves the authenticated user profile from InstantCard. |

