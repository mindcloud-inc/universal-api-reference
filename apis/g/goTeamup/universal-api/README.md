# <img src="https://images.mindcloud.co/apps/icons/go-teamup_1776104240154.png" alt="GoTeamup logo" width="28" height="28"> GoTeamup: Universal API

Fitness management software that helps businesses schedule classes, take payments, and manage the key parts of their operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/goTeamup/latest
- **Category:** Productivity / Scheduling
- **Actions:** 33
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://goteamup.com/
- **Vendor API docs:** https://docs.goteamup.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Providers](actions/list-providers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/list-providers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (33)

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [List Membership Categories](actions/list-membership-categories.md) | GET | Finds membership categories in GoTeamup. |
| [List Offering Types Helper](actions/list-offering-types-helper.md) | GET | Finds offering types in GoTeamup. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get Provider Entitlements](actions/get-provider-entitlements.md) | GET | Retrieves provider entitlements from GoTeamup. |
| [Retrieve Provider](actions/retrieve-provider.md) | GET | Retrieves a provider from GoTeamup. |

### Coupons

| Action | Method | Description |
| --- | --- | --- |
| [List Discount Codes](actions/list-discount-codes.md) | GET | Finds discount codes in GoTeamup. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in GoTeamup. |
| [List Customers](actions/list-customers.md) | GET | Finds customers in GoTeamup. |
| [Retrieve Customer](actions/retrieve-customer.md) | GET | Retrieves a customer from GoTeamup. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in GoTeamup. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [List Waivers](actions/list-waivers.md) | GET | Finds waivers in GoTeamup. |

### Employees

| Action | Method | Description |
| --- | --- | --- |
| [List Instructors](actions/list-instructors.md) | GET | Finds instructors in GoTeamup. |
| [Retrieve Instructor](actions/retrieve-instructor.md) | GET | Retrieves an instructor from GoTeamup. |
| [Retrieve Instructor Availability](actions/retrieve-instructor-availability.md) | GET | Retrieves instructor availability from GoTeamup. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [List Events](actions/list-events.md) | GET | Finds events in GoTeamup. |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [List Customer Forms](actions/list-customer-forms.md) | GET | Finds customer forms in GoTeamup. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [List Venues](actions/list-venues.md) | GET | Finds venues in GoTeamup. |

### Memberships

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Customer Membership](actions/cancel-customer-membership.md) | PUT | Cancels an existing customer membership in GoTeamup. |
| [Create Customer Membership](actions/create-customer-membership.md) | POST | Creates a new customer membership in GoTeamup. |
| [Create Membership](actions/create-membership.md) | POST | Creates a new membership in GoTeamup. |
| [Get Customer Membership Usage](actions/get-customer-membership-usage.md) | GET | Retrieves customer membership usage from GoTeamup. |
| [Get Membership Allotment](actions/get-membership-allotment.md) | GET | Retrieves membership allotment details from GoTeamup. |
| [List Customer Memberships](actions/list-customer-memberships.md) | GET | Finds customer memberships in GoTeamup. |
| [List Memberships](actions/list-memberships.md) | GET | Finds memberships in GoTeamup. |
| [Retrieve Customer Membership](actions/retrieve-customer-membership.md) | GET | Retrieves a customer membership from GoTeamup. |
| [Retrieve Membership](actions/retrieve-membership.md) | GET | Retrieves a membership from GoTeamup. |
| [Update Membership](actions/update-membership.md) | PUT | Updates an existing membership in GoTeamup. |

### Offering Type

| Action | Method | Description |
| --- | --- | --- |
| [Create Offering Type Helper](actions/create-offering-type-helper.md) | POST | Creates a new offering type in GoTeamup. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Create Order](actions/create-order.md) | POST | Creates a new order in GoTeamup. |
| [List Orders](actions/list-orders.md) | GET | Finds orders in GoTeamup. |
| [Retrieve Order](actions/retrieve-order.md) | GET | Retrieves an order from GoTeamup. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [List Products](actions/list-products.md) | GET | Finds products in GoTeamup. |

### Provider

| Action | Method | Description |
| --- | --- | --- |
| [List Providers](actions/list-providers.md) | GET | Finds providers in GoTeamup. |

### Venue

| Action | Method | Description |
| --- | --- | --- |
| [List Venues Helper](actions/list-venues-helper.md) | GET | Finds venues in GoTeamup. |

