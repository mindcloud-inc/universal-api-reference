# <img src="https://images.mindcloud.co/apps/icons/recreationgov_1776271257020.png" alt="Recreation.gov logo" width="28" height="28"> Recreation.gov: Universal API

Official API wrapper for Recreation.gov RIDB and developer-portal APIs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/recreationgov/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://ridb.recreation.gov/docs
- **Vendor API docs:** https://ridb.recreation.gov/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Public Organizations](actions/list-public-organizations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recreationgov/latest/actions/list-public-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Facility

| Action | Method | Description |
| --- | --- | --- |
| [Create Facility](actions/create-facility.md) | POST | Creates a new facility in Recreation.gov. |
| [Get Facility](actions/get-facility.md) | GET | Retrieves a facility from Recreation.gov. |
| [Update Facility](actions/update-facility.md) | PUT | Updates an existing facility in Recreation.gov. |

### Facility Activity

| Action | Method | Description |
| --- | --- | --- |
| [Create Facility Activity](actions/create-facility-activity.md) | POST | Creates a facility activity in Recreation.gov. |
| [List Facility Activities](actions/list-facility-activities.md) | GET | Retrieves activities for a facility from Recreation.gov. |
| [Update Facility Activity](actions/update-facility-activity.md) | PUT | Updates a facility activity in Recreation.gov. |

### Facility Address

| Action | Method | Description |
| --- | --- | --- |
| [Create Facility Address](actions/create-facility-address.md) | POST | Creates a facility address in Recreation.gov. |
| [List Facility Addresses](actions/list-facility-addresses.md) | GET | Retrieves addresses for a facility from Recreation.gov. |
| [Update Facility Address](actions/update-facility-address.md) | PUT | Updates a facility address in Recreation.gov. |

### Public Activity

| Action | Method | Description |
| --- | --- | --- |
| [List Public Activities](actions/list-public-activities.md) | GET |  |

### Public Asset

| Action | Method | Description |
| --- | --- | --- |
| [List Public Assets](actions/list-public-assets.md) | GET |  |

### Public Organization

| Action | Method | Description |
| --- | --- | --- |
| [List Public Organizations](actions/list-public-organizations.md) | GET |  |

### Rec Area

| Action | Method | Description |
| --- | --- | --- |
| [Create Rec Area](actions/create-rec-area.md) | POST | Creates a new recreation area in Recreation.gov. |
| [Get Rec Area](actions/get-rec-area.md) | GET | Retrieves a recreation area from Recreation.gov. |
| [Update Rec Area](actions/update-rec-area.md) | PUT | Updates an existing recreation area in Recreation.gov. |

### Rec Area Activity

| Action | Method | Description |
| --- | --- | --- |
| [Create Rec Area Activity](actions/create-rec-area-activity.md) | POST | Creates a recreation area activity in Recreation.gov. |
| [List Rec Area Activities](actions/list-rec-area-activities.md) | GET | Retrieves activities for a recreation area from Recreation.gov. |
| [Update Rec Area Activity](actions/update-rec-area-activity.md) | PUT | Updates a recreation area activity in Recreation.gov. |

### Rec Area Address

| Action | Method | Description |
| --- | --- | --- |
| [Create Rec Area Address](actions/create-rec-area-address.md) | POST | Creates a recreation area address in Recreation.gov. |
| [List Rec Area Addresses](actions/list-rec-area-addresses.md) | GET | Retrieves addresses for a recreation area from Recreation.gov. |
| [Update Rec Area Address](actions/update-rec-area-address.md) | PUT | Updates a recreation area address in Recreation.gov. |

### Rec Area Event

| Action | Method | Description |
| --- | --- | --- |
| [Create Rec Area Event](actions/create-rec-area-event.md) | POST | Creates a recreation area event in Recreation.gov. |
| [List Rec Area Events](actions/list-rec-area-events.md) | GET | Retrieves events for a recreation area from Recreation.gov. |
| [Update Rec Area Event](actions/update-rec-area-event.md) | PUT | Updates a recreation area event in Recreation.gov. |

