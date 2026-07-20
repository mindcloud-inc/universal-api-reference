# <img src="https://images.mindcloud.co/apps/icons/perkicon_1777065378291.png" alt="TravelPerk logo" width="28" height="28"> TravelPerk: Universal API

Manage TravelPerk invoices, trips, bookings, users, and cost centers

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/travelPerk/latest
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.perk.com
- **Vendor API docs:** https://developers.perk.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Invoice Lines](actions/list-invoice-lines.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/travelPerk/latest/actions/list-invoice-lines?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Cost Centers

| Action | Method | Description |
| --- | --- | --- |
| [Assign Users to Cost Center](actions/assign-users-to-cost-center.md) | PUT | Assigns users to a cost center in TravelPerk. |
| [Create Cost Center](actions/create-cost-center.md) | POST | Creates a new cost center in TravelPerk. |
| [Get Cost Center](actions/get-cost-center.md) | GET | Retrieves a cost center from TravelPerk. |
| [List Cost Centers](actions/list-cost-centers.md) | GET | Retrieves cost centers from TravelPerk. |
| [Update Cost Center](actions/update-cost-center.md) | PUT | Updates an existing cost center in TravelPerk. |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [Get Trip Custom Fields](actions/get-trip-custom-fields.md) | GET | Retrieves trip custom fields from TravelPerk. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Get Invoice PDF](actions/get-invoice-pdf.md) | GET | Retrieves an invoice PDF from TravelPerk. |

### Invoice Lines

| Action | Method | Description |
| --- | --- | --- |
| [List Invoice Lines](actions/list-invoice-lines.md) | GET | Retrieves invoice lines from TravelPerk. |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Get Invoice](actions/get-invoice.md) | GET | Retrieves an invoice from TravelPerk. |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices from TravelPerk. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Trip](actions/get-trip.md) | GET | Retrieves a trip from TravelPerk. |
| [List Bookings](actions/list-bookings.md) | GET | Retrieves booking information from TravelPerk. |
| [List Invoice Profiles](actions/list-invoice-profiles.md) | GET | Retrieves invoice profiles from TravelPerk. |
| [List Trips](actions/list-trips.md) | GET | Retrieves trips from TravelPerk. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create SCIM User](actions/create-scim-user.md) | POST | Creates a new SCIM user in TravelPerk. |
| [Delete SCIM User](actions/delete-scim-user.md) | DELETE | Deletes an existing SCIM user from TravelPerk. |
| [Get SCIM User](actions/get-scim-user.md) | GET | Retrieves a SCIM user from TravelPerk. |
| [List SCIM Users](actions/list-scim-users.md) | GET | Retrieves SCIM users from TravelPerk. |
| [List Users](actions/list-users.md) | GET | Retrieves user information from TravelPerk. |
| [Update SCIM User](actions/update-scim-user.md) | PUT | Updates an existing SCIM user in TravelPerk. |

