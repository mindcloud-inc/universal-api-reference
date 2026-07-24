# <img src="https://images.mindcloud.co/apps/icons/hub-spot-new_1772820785990.png" alt="HubSpot logo" width="28" height="28"> HubSpot: Universal API

Manage contacts, track deals, run campaigns, and support customers.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hubspotApp/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 74
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.hubspot.com/
- **Vendor API docs:** https://developers.hubspot.com/docs/api-reference/latest/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contacts](actions/list-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (74)

### Account Info

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Info](actions/get-account-info.md) | GET | Retrieves account details from HubSpot. |

### Association

| Action | Method | Description |
| --- | --- | --- |
| [Delete Association](actions/delete-association.md) | DELETE | Deletes an association between HubSpot records. |
| [List Associations](actions/list-associations.md) | GET | Retrieves associations for a HubSpot record. |

### Business Unit

| Action | Method | Description |
| --- | --- | --- |
| [List Business Units for User](actions/list-business-units-for-user.md) | GET | Retrieves business units for a HubSpot user. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Delete Company by ID](actions/delete-company-by-id.md) | DELETE | Deletes an existing company from HubSpot. |
| [Get Company by ID](actions/get-company-by-id.md) | GET | Retrieves a company from HubSpot by ID. |
| [List Companies](actions/list-companies.md) | GET | Retrieves companies from HubSpot. |
| [List Contact Companies](actions/list-contact-companies.md) | GET | Retrieves companies associated with a HubSpot contact. |
| [Search Companies](actions/search-companies.md) | GET | Finds companies in HubSpot. |
| [Update Company by ID](actions/update-company-by-id.md) | PUT | Updates an existing company in HubSpot. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Batch Read Contacts](actions/batch-read-contacts.md) | GET | Retrieves contacts from HubSpot in a batch. |
| [Delete Contact by ID](actions/delete-contact-by-id.md) | DELETE | Deletes an existing contact from HubSpot. |
| [Get Contact by ID](actions/get-contact-by-id.md) | GET | Retrieves a contact from HubSpot by ID. |
| [Get Listing By ID](actions/get-listing-by-id.md) | GET | Retrieves a listing from HubSpot by ID. |
| [List Company Contacts](actions/list-company-contacts.md) | GET | Retrieves contacts associated with a HubSpot company. |
| [List Company Contacts v2026-03](actions/list-company-contacts-v202603.md) | GET | Retrieves company contacts from HubSpot using the 2026-03 API. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from HubSpot. |
| [Search Contacts](actions/search-contacts.md) | GET | Finds contacts in HubSpot. |
| [Search Files](actions/search-files.md) | GET | Finds files in HubSpot. |
| [Update Contact by ID](actions/update-contact-by-id.md) | PUT | Updates an existing contact in HubSpot. |
| [Upload Files](actions/upload-files.md) | GET | Uploads a file to HubSpot. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in HubSpot. |

### Custom Object

| Action | Method | Description |
| --- | --- | --- |
| [Update Custom Object Record](actions/update-custom-object-record.md) | PUT | Updates a custom object record in HubSpot. |

### Deal

| Action | Method | Description |
| --- | --- | --- |
| [Create Deal](actions/create-deal.md) | POST | Creates a new deal in HubSpot. |
| [Update Deal by ID](actions/update-deal-by-id.md) | PUT | Updates an existing deal in HubSpot. |

### Deals

| Action | Method | Description |
| --- | --- | --- |
| [Get Deal by ID](actions/get-deal-by-id.md) | GET | Retrieves a deal from HubSpot by ID. |
| [List Deals](actions/list-deals.md) | GET | Retrieves deals from HubSpot. |
| [Search Deals](actions/search-deals.md) | GET | Finds deals in HubSpot. |

### Email

| Action | Method | Description |
| --- | --- | --- |
| [Get Email](actions/get-email.md) | GET | Retrieves an email activity from HubSpot by ID. |
| [List Emails](actions/list-emails.md) | GET | Retrieves email activities from HubSpot. |

### Engagement

| Action | Method | Description |
| --- | --- | --- |
| [Batch Read Engagements](actions/batch-read-engagements.md) | GET | Retrieves engagement records from HubSpot in a batch. |
| [Create Engagement](actions/create-engagement.md) | POST | Creates a new engagement record in HubSpot. |
| [Search Engagements](actions/search-engagements.md) | GET | Finds engagement records in HubSpot. |
| [Update Engagement by ID](actions/update-engagement-by-id.md) | PUT | Updates an existing engagement record in HubSpot. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Get File Details](actions/get-file-details.md) | GET | Retrieves file details from HubSpot. |

### Form

| Action | Method | Description |
| --- | --- | --- |
| [List Forms](actions/list-forms.md) | GET | Retrieves forms from HubSpot. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Search Invoices](actions/search-invoices.md) | GET | Finds invoices in HubSpot. |
| [Update Invoice by ID](actions/update-invoice-by-id.md) | PUT | Updates an existing invoice in HubSpot. |

### Line Item

| Action | Method | Description |
| --- | --- | --- |
| [Batch Read Line Items](actions/batch-read-line-items.md) | GET | Retrieves line items from HubSpot in a batch. |
| [Create Line Item](actions/create-line-item.md) | POST | Creates a new line item in HubSpot. |
| [List Deal Line Items](actions/list-deal-line-items.md) | GET | Retrieves line items associated with a HubSpot deal. |

### List

| Action | Method | Description |
| --- | --- | --- |
| [Create List](actions/create-list.md) | POST | Creates a new list in HubSpot. |
| [Search Lists](actions/search-lists.md) | GET | Finds lists in HubSpot. |

### Note

| Action | Method | Description |
| --- | --- | --- |
| [Batch Read Notes](actions/batch-read-notes.md) | GET | Retrieves notes from HubSpot in a batch. |

### Object Schema

| Action | Method | Description |
| --- | --- | --- |
| [Create Object Schema](actions/create-object-schema.md) | POST | Creates a new object schema in HubSpot. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Batch Create Orders](actions/batch-create-orders.md) | POST | Creates new orders in HubSpot in a batch. |
| [Search Orders](actions/search-orders.md) | GET | Finds orders in HubSpot. |

### Owner

| Action | Method | Description |
| --- | --- | --- |
| [Get Owner](actions/get-owner.md) | GET | Retrieves an owner from HubSpot by ID. |
| [List Owners](actions/list-owners.md) | GET | Retrieves owners from HubSpot. |

### Pipeline

| Action | Method | Description |
| --- | --- | --- |
| [Get Pipeline by ID](actions/get-pipeline-by-id.md) | GET | Retrieves a pipeline from HubSpot by ID. |
| [List Pipelines](actions/list-pipelines.md) | GET | Retrieves pipelines from HubSpot. |

### Pipeline Stage

| Action | Method | Description |
| --- | --- | --- |
| [Create Pipeline Stage](actions/create-pipeline-stage.md) | POST |  |
| [Get Pipeline Stage by ID](actions/get-pipeline-stage-by-id.md) | GET | Retrieves a pipeline stage from HubSpot by ID. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a new product in HubSpot. |
| [Search Products](actions/search-products.md) | GET | Finds products in HubSpot. |

### Property

| Action | Method | Description |
| --- | --- | --- |
| [Create Property](actions/create-property.md) | POST | Creates a new property in HubSpot. |
| [Delete Property](actions/delete-property.md) | DELETE | Deletes an existing property from HubSpot. |
| [Get Company Industries](actions/get-company-industries.md) | GET | Retrieves the company industry property from HubSpot. |
| [Get Property Details](actions/get-property-details.md) | GET | Retrieves property details from HubSpot. |
| [Get Shipping Method](actions/get-shipping-method.md) | GET | Retrieves the shipping method property from HubSpot. |
| [List Properties](actions/list-properties.md) | GET | Retrieves properties from HubSpot. |

### Quote

| Action | Method | Description |
| --- | --- | --- |
| [Create Quote](actions/create-quote.md) | POST | Creates a new quote in HubSpot. |
| [Get Quote by ID](actions/get-quote-by-id.md) | GET | Retrieves a quote from HubSpot by ID. |
| [List Deal Quotes](actions/list-deal-quotes.md) | GET | Retrieves quotes associated with a HubSpot deal. |

### Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [Get Subscription by ID](actions/get-subscription-by-id.md) | GET |  |
| [List Subscriptions](actions/list-subscriptions.md) | GET |  |
| [Search Subscriptions](actions/search-subscriptions.md) | GET |  |

### Ticket

| Action | Method | Description |
| --- | --- | --- |
| [Delete Ticket by ID](actions/delete-ticket-by-id.md) | DELETE | Deletes an existing ticket from HubSpot. |

### Tickets

| Action | Method | Description |
| --- | --- | --- |
| [Get Ticket by ID](actions/get-ticket-by-id.md) | GET | Retrieves a ticket from HubSpot by ID. |
| [List Tickets](actions/list-tickets.md) | GET | Retrieves tickets from HubSpot. |
| [Search Tickets](actions/search-tickets.md) | GET | Finds tickets in HubSpot. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Add User](actions/add-user.md) | POST | Creates a new user in HubSpot. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from HubSpot by ID. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves users from HubSpot. |

