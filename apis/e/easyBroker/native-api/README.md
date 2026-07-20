# EasyBroker: Native API Reference

A consolidated summary of EasyBroker's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://dev.easybroker.com/reference
- **API base URL:** `https://api.easybroker.com/v1`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Authorization: <apiKey>
```

[Official authentication documentation](https://dev.easybroker.com/docs/autenticaci%C3%B3n)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `content`. The next-page cursor is read from `pagination.next_page`. The current page number is read from `pagination.page`.

## Pagination

Use `limit` in the query string to set the page size (default 20). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contact Request](actions/create-contact-request.md) | `POST /contact_requests` | [docs](https://dev.easybroker.com/reference/post_contact-requests) |
| [Create Partner Contact Request](actions/create-partner-contact-request.md) | `POST /integration_partners/contact_requests` | [docs](https://dev.easybroker.com/reference/post_contact-requests-1) |
| [Create Property](actions/create-property.md) | `POST /properties` | [docs](https://dev.easybroker.com/reference/post_properties) |
| [List Agencies](actions/list-agencies.md) | `GET /integration_partners/agencies` | [docs](https://dev.easybroker.com/reference/get_agencies) |
| [List Collaborations](actions/list-collaborations.md) | `GET /collaborations` | [docs](https://dev.easybroker.com/reference/get_collaborations) |
| [List Contact Requests](actions/list-contact-requests.md) | `GET /contact_requests` | [docs](https://dev.easybroker.com/reference/get_contact-requests) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://dev.easybroker.com/reference/get_contacts) |
| [List MLS Properties](actions/list-mls-properties.md) | `GET /mls_properties` | [docs](https://dev.easybroker.com/reference/get_mls-properties) |
| [List Partner Contact Requests](actions/list-partner-contact-requests.md) | `GET /integration_partners/contact_requests` | [docs](https://dev.easybroker.com/reference/get_contact-requests-1) |
| [List Partner Property Listing Statuses](actions/list-partner-property-listing-statuses.md) | `GET /integration_partners/listing_statuses` | [docs](https://dev.easybroker.com/reference/get_listing-statuses-1) |
| [List Properties](actions/list-properties.md) | `GET /properties` | [docs](https://dev.easybroker.com/reference/get_properties) |
| [List Property Features](actions/list-property-features.md) | `GET /features` | [docs](https://dev.easybroker.com/reference/get_features) |
| [List Property Listing Statuses](actions/list-property-listing-statuses.md) | `GET /listing_statuses` | [docs](https://dev.easybroker.com/reference/get_listing-statuses) |
| [List Property Types](actions/list-property-types.md) | `GET /property_types` | [docs](https://dev.easybroker.com/reference/get_property-types) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://dev.easybroker.com/reference/get_users) |
| [Retrieve Agency](actions/retrieve-agency.md) | `GET /integration_partners/agencies/:agency_id` | [docs](https://dev.easybroker.com/reference/get_agencies-agency-id) |
| [Retrieve Agent](actions/retrieve-agent.md) | `GET /integration_partners/agents/:agent_id` | [docs](https://dev.easybroker.com/reference/get_agents-agent-id) |
| [Retrieve Contact](actions/retrieve-contact.md) | `GET /contacts/{contact_id}` | [docs](https://dev.easybroker.com/reference/get_contacts-contact-id) |
| [Retrieve Location](actions/retrieve-location.md) | `GET /locations` | [docs](https://dev.easybroker.com/reference/get_locations) |
| [Retrieve MLS Property](actions/retrieve-mls-property.md) | `GET /mls_properties/:property_id` | [docs](https://dev.easybroker.com/reference/get_mls-properties-property-id) |
| [Retrieve Partner Property](actions/retrieve-partner-property.md) | `GET /integration_partners/properties/:property_id` | [docs](https://dev.easybroker.com/reference/get_properties-property-id-1) |
| [Retrieve Property](actions/retrieve-property.md) | `GET /properties/{property_id}` | [docs](https://dev.easybroker.com/reference/get_properties-property-id) |
| [Update Agency Integration](actions/update-agency-integration.md) | `PATCH /integration_partners/agencies/:agency_id/integration` | [docs](https://dev.easybroker.com/reference/patch_agencies-agency-id-integration) |
| [Update Property](actions/update-property.md) | `PATCH /properties/{property_id}` | [docs](https://dev.easybroker.com/reference/patch_properties-property-id) |
| [Update Property Integration](actions/update-property-integration.md) | `PATCH /integration_partners/properties/:property_id/property_integration` | [docs](https://dev.easybroker.com/reference/patch_properties-property-id-property-integration) |
