# <img src="https://images.mindcloud.co/apps/icons/serviceminder_1782741161502.png" alt="serviceminder.io logo" width="28" height="28"> serviceminder.io: Universal API

ServiceMinder is a field-service and franchise management platform for scheduling, contacts, proposals, invoices, and service operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/serviceminderio/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 35
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://serviceminder.com/
- **Vendor API docs:** https://serviceminder.io/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Test Echo](actions/test-echo.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/test-echo?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (35)

### Appointment

| Action | Method | Description |
| --- | --- | --- |
| [Find Appointment](actions/find-appointment.md) | GET | Retrieves an appointment from ServiceMinder by ID. |
| [Query Appointments](actions/query-appointments.md) | GET | Finds appointments in ServiceMinder by date, contact, or agent. |

### Appointment Slot

| Action | Method | Description |
| --- | --- | --- |
| [Search Appointment Slots](actions/search-appointment-slots.md) | GET | Finds appointment slots in ServiceMinder by date range and service. |

### Blog

| Action | Method | Description |
| --- | --- | --- |
| [Find Blogs](actions/find-blogs.md) | GET | Finds blogs in ServiceMinder by search term. |
| [Get Blog](actions/get-blog.md) | GET | Retrieves a blog from ServiceMinder. |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [List Channel Campaigns](actions/list-channel-campaigns.md) | GET | Retrieves channel campaigns from ServiceMinder. |

### Cancel Reason

| Action | Method | Description |
| --- | --- | --- |
| [List Cancel Reasons](actions/list-cancel-reasons.md) | GET | Retrieves cancel reasons from ServiceMinder. |

### Channel

| Action | Method | Description |
| --- | --- | --- |
| [List Channels](actions/list-channels.md) | GET | Retrieves channels from ServiceMinder. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Search Contacts](actions/search-contacts.md) | GET | Finds contacts in ServiceMinder by name, email, phone, or address. |

### Contact Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Contact Tags](actions/list-contact-tags.md) | GET | Retrieves tags for a contact from ServiceMinder. |

### Custom Field

| Action | Method | Description |
| --- | --- | --- |
| [List Custom Fields](actions/list-custom-fields.md) | GET | Retrieves custom fields from ServiceMinder. |

### Data Subscriber Download

| Action | Method | Description |
| --- | --- | --- |
| [Get Data Subscriber Download](actions/get-data-subscriber-download.md) | GET | Retrieves a data subscriber download from ServiceMinder. |

### Data Subscriber Event

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Data Subscriber Events](actions/fetch-data-subscriber-events.md) | GET | Retrieves data subscriber events from ServiceMinder. |

### Data Subscriber Forecast

| Action | Method | Description |
| --- | --- | --- |
| [Get Data Subscriber Forecasts](actions/get-data-subscriber-forecasts.md) | GET | Retrieves data subscriber forecasts from ServiceMinder. |

### Download

| Action | Method | Description |
| --- | --- | --- |
| [Get Download](actions/get-download.md) | GET | Retrieves a download from ServiceMinder. |

### Feature

| Action | Method | Description |
| --- | --- | --- |
| [List Features](actions/list-features.md) | GET | Retrieves available features from ServiceMinder. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Get Invoice](actions/get-invoice.md) | GET | Retrieves an invoice from ServiceMinder by ID. |
| [Query Invoices](actions/query-invoices.md) | GET | Finds invoices in ServiceMinder by date range. |

### Lead Source Category

| Action | Method | Description |
| --- | --- | --- |
| [List Lead Source Categories](actions/list-lead-source-categories.md) | GET | Retrieves lead source categories from ServiceMinder. |

### Named Tax Rate

| Action | Method | Description |
| --- | --- | --- |
| [List Named Tax Rates](actions/list-named-tax-rates.md) | GET | Retrieves named tax rates from ServiceMinder. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization Details](actions/get-organization-details.md) | GET | Retrieves organization details from ServiceMinder. |
| [Query Organizations](actions/query-organizations.md) | GET | Finds organizations in ServiceMinder by name. |

### Part

| Action | Method | Description |
| --- | --- | --- |
| [Get Part Details](actions/get-part-details.md) | GET | Retrieves part details from ServiceMinder. |

### Part Dimension

| Action | Method | Description |
| --- | --- | --- |
| [Get Part Dimensions](actions/get-part-dimensions.md) | GET | Retrieves part dimensions from ServiceMinder. |

### Payment

| Action | Method | Description |
| --- | --- | --- |
| [Query Payments](actions/query-payments.md) | GET | Finds payments in ServiceMinder by date range. |

### Proposal

| Action | Method | Description |
| --- | --- | --- |
| [Get Proposal Details](actions/get-proposal-details.md) | GET | Retrieves proposal details from ServiceMinder. |
| [Query Proposals](actions/query-proposals.md) | GET | Finds proposals in ServiceMinder by date range. |

### Proposal Template

| Action | Method | Description |
| --- | --- | --- |
| [List Proposal Templates](actions/list-proposal-templates.md) | GET | Retrieves proposal templates from ServiceMinder. |

### Radius City

| Action | Method | Description |
| --- | --- | --- |
| [List Radius Cities](actions/list-radius-cities.md) | GET | Retrieves radius cities from ServiceMinder. |

### Radius Postal Code

| Action | Method | Description |
| --- | --- | --- |
| [List Radius Postal Codes](actions/list-radius-postal-codes.md) | GET | Retrieves radius postal codes from ServiceMinder. |

### Service

| Action | Method | Description |
| --- | --- | --- |
| [Get Service Details](actions/get-service-details.md) | GET | Retrieves service details from ServiceMinder. |
| [List Services](actions/list-services.md) | GET | Retrieves services from ServiceMinder. |

### Service Agent

| Action | Method | Description |
| --- | --- | --- |
| [List Service Agents](actions/list-service-agents.md) | GET | Retrieves service agents from ServiceMinder. |

### Test Echo

| Action | Method | Description |
| --- | --- | --- |
| [Test Echo](actions/test-echo.md) | GET | Retrieves a test echo response from ServiceMinder. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves users from ServiceMinder. |

