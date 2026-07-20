# <img src="https://images.mindcloud.co/apps/icons/easy-broker_1773944644173.png" alt="EasyBroker logo" width="28" height="28"> EasyBroker: Universal API

Manage properties, contacts, and listings in EasyBroker

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/easyBroker/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.easybroker.com
- **Vendor API docs:** https://dev.easybroker.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Property Types](actions/list-property-types.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyBroker/latest/actions/list-property-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Agency

| Action | Method | Description |
| --- | --- | --- |
| [List Agencies](actions/list-agencies.md) | GET | Retrieves active partner agencies from EasyBroker. |
| [Retrieve Agency](actions/retrieve-agency.md) | GET | Retrieves a connected agency from EasyBroker. |

### Agency Integration

| Action | Method | Description |
| --- | --- | --- |
| [Update Agency Integration](actions/update-agency-integration.md) | PUT | Updates an agency integration status in EasyBroker. |

### Agent

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Agent](actions/retrieve-agent.md) | GET | Retrieves an agent from EasyBroker. |

### Collaboration

| Action | Method | Description |
| --- | --- | --- |
| [List Collaborations](actions/list-collaborations.md) | GET | Retrieves collaborations from EasyBroker. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from EasyBroker. |
| [Retrieve Contact](actions/retrieve-contact.md) | GET | Retrieves a contact from EasyBroker. |

### Contact Request

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact Request](actions/create-contact-request.md) | POST | Creates or updates a property contact request in EasyBroker. |
| [List Contact Requests](actions/list-contact-requests.md) | GET | Retrieves contact requests from EasyBroker. |

### Listing Status

| Action | Method | Description |
| --- | --- | --- |
| [List Property Listing Statuses](actions/list-property-listing-statuses.md) | GET | Retrieves property listing statuses from EasyBroker. |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Location](actions/retrieve-location.md) | GET | Retrieves location details from EasyBroker. |

### Mls Property

| Action | Method | Description |
| --- | --- | --- |
| [List MLS Properties](actions/list-mls-properties.md) | GET | Retrieves MLS properties from EasyBroker. |
| [Retrieve MLS Property](actions/retrieve-mls-property.md) | GET | Retrieves an MLS property from EasyBroker. |

### Partner Contact Request

| Action | Method | Description |
| --- | --- | --- |
| [Create Partner Contact Request](actions/create-partner-contact-request.md) | POST | Creates a partner contact request in EasyBroker. |
| [List Partner Contact Requests](actions/list-partner-contact-requests.md) | GET | Retrieves partner contact requests from EasyBroker. |

### Partner Listing Status

| Action | Method | Description |
| --- | --- | --- |
| [List Partner Property Listing Statuses](actions/list-partner-property-listing-statuses.md) | GET | Retrieves partner property listing statuses from EasyBroker. |

### Partner Property

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Partner Property](actions/retrieve-partner-property.md) | GET | Retrieves a property linked to your integration in EasyBroker. |

### Property

| Action | Method | Description |
| --- | --- | --- |
| [Create Property](actions/create-property.md) | POST | Creates a new property in EasyBroker. |
| [List Properties](actions/list-properties.md) | GET | Retrieves properties from EasyBroker. |
| [Retrieve Property](actions/retrieve-property.md) | GET | Retrieves a property from EasyBroker. |
| [Update Property](actions/update-property.md) | PUT | Updates an existing property in EasyBroker. |

### Property Feature

| Action | Method | Description |
| --- | --- | --- |
| [List Property Features](actions/list-property-features.md) | GET | Retrieves property features from EasyBroker. |

### Property Integration

| Action | Method | Description |
| --- | --- | --- |
| [Update Property Integration](actions/update-property-integration.md) | PUT | Updates a property integration status in EasyBroker. |

### Property Type

| Action | Method | Description |
| --- | --- | --- |
| [List Property Types](actions/list-property-types.md) | GET | Retrieves property types from EasyBroker. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves active users from EasyBroker. |

