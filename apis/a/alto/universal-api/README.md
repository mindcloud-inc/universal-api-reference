# <img src="https://images.mindcloud.co/apps/icons/alto_1776796431716.png" alt="Alto logo" width="28" height="28"> Alto: Universal API

Alto is a cloud-based estate agency and property-management platform for UK sales, lettings, contacts, tenancies, appointments, documents, and related branch operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/alto/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.altosoftware.co.uk/
- **Vendor API docs:** https://developers.vebraalto.com/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Branches](actions/get-branches.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-branches?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Appointment

| Action | Method | Description |
| --- | --- | --- |
| [Get Appointment](actions/get-appointment.md) | GET | Retrieves an appointment from Alto by ID and instance. |
| [Get Negotiator Appointments](actions/get-negotiator-appointments.md) | GET | Retrieves negotiator appointments from Alto within a selected time range. |

### Branch

| Action | Method | Description |
| --- | --- | --- |
| [Get Branch](actions/get-branch.md) | GET | Retrieves a branch from Alto by ID. |
| [Get Branches](actions/get-branches.md) | GET | Retrieves branch records from your Alto account. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Get All Contacts](actions/get-all-contacts.md) | GET | Retrieves all contact records from your Alto account. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Alto by ID. |
| [Get Contacts](actions/get-contacts.md) | GET | Retrieves contacts from Alto by IDs. |
| [Search Contacts](actions/search-contacts.md) | GET | Finds contacts in Alto by search criteria. |

### Contact Relationship

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact Relationships](actions/get-contact-relationships.md) | GET | Retrieves contact relationships from Alto by contact ID. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Get Documents](actions/get-documents.md) | GET | Finds documents in Alto by linked record or media type. |
| [Get Inventory Documents](actions/get-inventory-documents.md) | GET | Retrieves documents for an inventory item in Alto. |

### Document Content

| Action | Method | Description |
| --- | --- | --- |
| [Get Document Content](actions/get-document-content.md) | GET | Retrieves document content from Alto by document ID. |

### Inventory Item

| Action | Method | Description |
| --- | --- | --- |
| [Filter Inventory](actions/filter-inventory.md) | GET | Finds inventory items in Alto by filter criteria. |
| [Get Inventory](actions/get-inventory.md) | GET | Retrieves inventory records from your Alto account. |
| [Get Inventory Item](actions/get-inventory-item.md) | GET | Retrieves an inventory item from Alto by ID. |
| [Get Inventory Items](actions/get-inventory-items.md) | GET | Retrieves inventory items from Alto by IDs. |
| [Search Inventory](actions/search-inventory.md) | GET | Finds inventory items in Alto by search criteria. |

### Landlord

| Action | Method | Description |
| --- | --- | --- |
| [Get Inventory Landlords](actions/get-inventory-landlords.md) | GET | Retrieves landlords for an inventory item in Alto. |
| [Get Landlords](actions/get-landlords.md) | GET | Retrieves landlord records from your Alto account. |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Get Lead](actions/get-lead.md) | GET | Retrieves a lead from Alto by ID. |
| [Get Leads](actions/get-leads.md) | GET | Retrieves lead records from your Alto account. |

### Marketing Preference

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact Marketing Preferences](actions/get-contact-marketing-preferences.md) | GET | Retrieves contact marketing preferences from Alto by contact ID. |

### Meter Reading

| Action | Method | Description |
| --- | --- | --- |
| [Get Tenancy Meter Readings](actions/get-tenancy-meter-readings.md) | GET | Retrieves tenancy meter readings from Alto. |

### Negotiator

| Action | Method | Description |
| --- | --- | --- |
| [Get Negotiator](actions/get-negotiator.md) | GET | Retrieves a negotiator from Alto by ID. |
| [Get Negotiators](actions/get-negotiators.md) | GET | Retrieves negotiator records from your Alto account. |

### Owner

| Action | Method | Description |
| --- | --- | --- |
| [Get Owners](actions/get-owners.md) | GET | Retrieves owner records from your Alto account. |

### Person

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact Person](actions/get-contact-person.md) | GET | Retrieves a contact person from Alto by contact and person ID. |
| [Get Contact Persons](actions/get-contact-persons.md) | GET | Retrieves contact persons from Alto by contact ID. |

### Property Image

| Action | Method | Description |
| --- | --- | --- |
| [Get Property Listing Images](actions/get-property-listing-images.md) | GET | Retrieves property image metadata from Alto. |

### Property Listing

| Action | Method | Description |
| --- | --- | --- |
| [Filter Listings](actions/filter-listings.md) | GET | Finds property listings in Alto by filter criteria. |
| [Get Property Listing](actions/get-property-listing.md) | GET | Retrieves a property listing from Alto by property ID. |
| [Get Property Listings](actions/get-property-listings.md) | GET | Retrieves property listings from Alto by property IDs. |

### Supplier

| Action | Method | Description |
| --- | --- | --- |
| [Get Supplier](actions/get-supplier.md) | GET | Retrieves a supplier from Alto by ID. |
| [Get Suppliers](actions/get-suppliers.md) | GET | Retrieves supplier records from your Alto account. |

### Tenancy

| Action | Method | Description |
| --- | --- | --- |
| [Get Inventory Tenancies](actions/get-inventory-tenancies.md) | GET | Retrieves tenancies for an inventory item in Alto. |
| [Get Tenancies](actions/get-tenancies.md) | GET | Retrieves tenancy records from your Alto account. |
| [Get Tenancy](actions/get-tenancy.md) | GET | Retrieves a tenancy from Alto by ID. |

### Tenant

| Action | Method | Description |
| --- | --- | --- |
| [Get Tenancy Tenant IDs](actions/get-tenancy-tenant-ids.md) | GET | Retrieves tenant IDs for a tenancy in Alto. |

### Valuation

| Action | Method | Description |
| --- | --- | --- |
| [Get Valuations](actions/get-valuations.md) | GET | Retrieves valuations from Alto by created date range. |

### Work Order

| Action | Method | Description |
| --- | --- | --- |
| [Get Work Order](actions/get-work-order.md) | GET | Retrieves a work order from Alto by ID. |

