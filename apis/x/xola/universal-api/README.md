# <img src="https://images.mindcloud.co/apps/icons/xola_1775248433383.png" alt="Xola logo" width="28" height="28"> Xola: Universal API

Manage bookings, availability, products, and guest payments in Xola

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/xola/latest
- **Category:** Marketing / Events & Webinars
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.xola.com
- **Vendor API docs:** https://developers.xola.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Experiences](actions/list-experiences.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xola/latest/actions/list-experiences?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Affiliate

| Action | Method | Description |
| --- | --- | --- |
| [Create Affiliate](actions/create-affiliate.md) | POST | Creates a new affiliate for a seller in Xola. |
| [Update Affiliate](actions/update-affiliate.md) | PUT | Updates an existing affiliate in Xola. |

### Availability

| Action | Method | Description |
| --- | --- | --- |
| [Get Batch Availability](actions/get-batch-availability.md) | GET | Retrieves batch availability from Xola. |
| [Get Experience Availability](actions/get-experience-availability.md) | GET | Retrieves availability for an experience from Xola. |

### Button

| Action | Method | Description |
| --- | --- | --- |
| [Create Button](actions/create-button.md) | POST | Creates a new button in Xola. |
| [List Buttons](actions/list-buttons.md) | GET | Finds buttons in Xola. |
| [Retrieve Button](actions/retrieve-button.md) | GET | Retrieves a button from Xola by ID. |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [List Categories](actions/list-categories.md) | GET | Finds categories in Xola. |

### Coupon

| Action | Method | Description |
| --- | --- | --- |
| [Create Coupon](actions/create-coupon.md) | POST | Creates a new coupon in Xola. |
| [List Coupons](actions/list-coupons.md) | GET | Finds coupons in Xola. |
| [Retrieve Coupon](actions/retrieve-coupon.md) | GET | Retrieves a coupon from Xola by ID. |

### Demographic

| Action | Method | Description |
| --- | --- | --- |
| [List Demographics](actions/list-demographics.md) | GET | Finds demographics in Xola. |
| [Retrieve Demographic](actions/retrieve-demographic.md) | GET | Retrieves a demographic from Xola by ID. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Create Event](actions/create-event.md) | POST | Creates a new event in Xola. |

### Experience

| Action | Method | Description |
| --- | --- | --- |
| [Create Experience](actions/create-experience.md) | POST | Creates a new experience in Xola. |
| [List Experiences](actions/list-experiences.md) | GET | Finds experiences in Xola. |

### Form

| Action | Method | Description |
| --- | --- | --- |
| [Create Form](actions/create-form.md) | POST | Creates a new form in Xola. |
| [List Forms](actions/list-forms.md) | GET | Finds forms in Xola. |
| [Retrieve Form](actions/retrieve-form.md) | GET | Retrieves a form from Xola by ID. |

### Gift

| Action | Method | Description |
| --- | --- | --- |
| [Create Gift](actions/create-gift.md) | POST | Creates a new gift in Xola. |
| [List Gifts](actions/list-gifts.md) | GET | Finds gifts in Xola. |

### Guide

| Action | Method | Description |
| --- | --- | --- |
| [Create Guide](actions/create-guide.md) | POST | Creates a new guide for a seller in Xola. |
| [List Guides](actions/list-guides.md) | GET | Finds guides for a seller in Xola. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Order](actions/retrieve-order.md) | GET | Retrieves an order from Xola by ID. |

### Order Form

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Order Form](actions/retrieve-order-form.md) | GET | Retrieves the form for an order in Xola. |

### Package

| Action | Method | Description |
| --- | --- | --- |
| [Create Package](actions/create-package.md) | POST | Creates a new package in Xola. |
| [List Packages](actions/list-packages.md) | GET | Finds packages in Xola. |
| [Update Package](actions/update-package.md) | PUT | Updates an existing package in Xola. |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [List Transactions](actions/list-transactions.md) | GET | Finds transactions in Xola. |
| [Retrieve Transaction](actions/retrieve-transaction.md) | GET | Retrieves a transaction from Xola by ID. |

