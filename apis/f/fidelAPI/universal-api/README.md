# <img src="https://images.mindcloud.co/apps/icons/idx2lt-dm-qz-1776704598783_1776704604253.png" alt="Fidel API logo" width="28" height="28"> Fidel API: Universal API

Link payment cards and monitor card transactions

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/fidelAPI/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.fidelapi.com
- **Vendor API docs:** https://docs.fidelapi.com/docs/select

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Brands](actions/list-brands.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/list-brands?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Brand

| Action | Method | Description |
| --- | --- | --- |
| [Create Brand](actions/create-brand.md) | POST | Creates a new brand in Fidel API. |
| [Get Brand](actions/get-brand.md) | GET | Retrieves a brand from Fidel API. |
| [List Brands](actions/list-brands.md) | GET | Retrieves brands from Fidel API. |
| [Update Brand](actions/update-brand.md) | PUT | Updates an existing brand in Fidel API. |

### Card

| Action | Method | Description |
| --- | --- | --- |
| [Create Card](actions/create-card.md) | POST | Creates a card in a Fidel program. |
| [Get Card](actions/get-card.md) | GET | Retrieves a card from Fidel API. |
| [List Cards](actions/list-cards.md) | GET | Retrieves cards from a Fidel program. |
| [Update Card Metadata](actions/update-card-metadata.md) | PUT | Updates metadata for a Fidel card. |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Create Location](actions/create-location.md) | POST | Creates a location in a Fidel program. |
| [Get Location](actions/get-location.md) | GET | Retrieves a location from Fidel API. |
| [List Locations](actions/list-locations.md) | GET | Retrieves locations from a Fidel program. |
| [List Locations by Brand](actions/list-locations-by-brand.md) | GET | Retrieves locations for a brand in Fidel API. |
| [Update Location](actions/update-location.md) | PUT | Updates an existing location in Fidel API. |

### Mid

| Action | Method | Description |
| --- | --- | --- |
| [List MIDs](actions/list-mids.md) | GET | Retrieves MIDs from a Fidel program. |

### Mid Request

| Action | Method | Description |
| --- | --- | --- |
| [Create MID Request](actions/create-mid-request.md) | POST | Creates a MID request in Fidel API. |

### Missing Transaction Request

| Action | Method | Description |
| --- | --- | --- |
| [Create Missing Transaction Request](actions/create-missing-transaction-request.md) | POST | Creates a missing transaction request in Fidel API. |

### Offer

| Action | Method | Description |
| --- | --- | --- |
| [Activate Offer on Card](actions/activate-offer-on-card.md) | POST | Activates an offer on a Fidel card. |
| [Create Offer](actions/create-offer.md) | POST | Creates a new offer in Fidel API. |
| [Get Offer](actions/get-offer.md) | GET | Retrieves an offer from Fidel API. |
| [Link Location to Offer](actions/link-location-to-offer.md) | POST | Links a location to an offer in Fidel API. |
| [List Offers](actions/list-offers.md) | GET | Retrieves offers from Fidel API. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook (Program)](actions/create-webhook-program.md) | POST | Creates a webhook for a Fidel program. |
| [Delete Offer](actions/delete-offer.md) | DELETE | Deletes an existing offer from Fidel API. |
| [Get MID](actions/get-mid.md) | GET | Retrieves a MID from a Fidel program. |
| [Get MID Request](actions/get-mid-request.md) | GET | Retrieves a MID request from Fidel API. |
| [Get Missing Transaction Request](actions/get-missing-transaction-request.md) | GET | Retrieves a missing transaction request from Fidel API. |
| [List MID Requests](actions/list-mid-requests.md) | GET | Retrieves MID requests from a Fidel program. |
| [List Missing Transaction Requests](actions/list-missing-transaction-requests.md) | GET | Retrieves missing transaction requests from a Fidel program. |
| [Update Offer](actions/update-offer.md) | PUT | Updates an existing offer in Fidel API. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in Fidel API. |

### Program

| Action | Method | Description |
| --- | --- | --- |
| [Create Program](actions/create-program.md) | POST | Creates a new program in Fidel API. |
| [Get Program](actions/get-program.md) | GET | Retrieves a program from Fidel API. |
| [List Programs](actions/list-programs.md) | GET | Retrieves programs from Fidel API. |
| [Sync Program](actions/sync-program.md) | PUT | Syncs an existing program in Fidel API. |
| [Update Program](actions/update-program.md) | PUT | Updates an existing program in Fidel API. |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Get Transaction](actions/get-transaction.md) | GET | Retrieves a transaction from Fidel API. |
| [List Transactions by Card](actions/list-transactions-by-card.md) | GET | Retrieves transactions for a Fidel card. |
| [List Transactions by Program](actions/list-transactions-by-program.md) | GET | Retrieves transactions for a Fidel program. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook from Fidel API. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from a Fidel program. |

