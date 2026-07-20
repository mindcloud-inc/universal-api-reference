# Recreation.gov: Native API Reference

A consolidated summary of Recreation.gov's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://ridb.recreation.gov/docs
- **API base URL:** `https://ridb.recreation.gov/api/v1`

## Authentication

### API Key

Vendor-issued RIDB API key required on every call.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://ridb.recreation.gov/access-agreement-ridb)

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–50). Use `offset` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `sort` in the query string. Only one sort field is accepted.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Facility](actions/create-facility.md) | `POST /facilities` | [docs](https://ridb.recreation.gov/shared/swagger/dataSteward.yaml) |
| [Create Facility Activity](actions/create-facility-activity.md) | `POST /facilities/{id}/activities` | [docs](https://ridb.recreation.gov/shared/swagger/dataSteward.yaml) |
| [Create Facility Address](actions/create-facility-address.md) | `POST /facilities/{id}/facilityaddresses` | [docs](https://ridb.recreation.gov/shared/swagger/dataSteward.yaml) |
| [Create Rec Area](actions/create-rec-area.md) | `POST /recareas` | [docs](https://ridb.recreation.gov/shared/swagger/dataSteward.yaml) |
| [Create Rec Area Activity](actions/create-rec-area-activity.md) | `POST /recareas/{id}/activities` | [docs](https://ridb.recreation.gov/shared/swagger/dataSteward.yaml) |
| [Create Rec Area Address](actions/create-rec-area-address.md) | `POST /recareas/{id}/recareaaddresses` | [docs](https://ridb.recreation.gov/shared/swagger/dataSteward.yaml) |
| [Create Rec Area Event](actions/create-rec-area-event.md) | `POST /recareas/{id}/events` | [docs](https://ridb.recreation.gov/shared/swagger/dataSteward.yaml) |
| [Get Facility](actions/get-facility.md) | `GET /facilities/{id}` | [docs](https://ridb.recreation.gov/shared/swagger/ridb.yaml) |
| [Get Rec Area](actions/get-rec-area.md) | `GET /recareas/{id}` | [docs](https://ridb.recreation.gov/shared/swagger/ridb.yaml) |
| [List Facility Activities](actions/list-facility-activities.md) | `GET /facilities/{id}/activities` | [docs](https://ridb.recreation.gov/shared/swagger/ridb.yaml) |
| [List Facility Addresses](actions/list-facility-addresses.md) | `GET /facilities/{id}/facilityaddresses` | [docs](https://ridb.recreation.gov/shared/swagger/ridb.yaml) |
| [List Public Activities](actions/list-public-activities.md) | `GET /public/activities` | [docs](https://ridb.recreation.gov/shared/swagger/ridb.yaml) |
| [List Public Assets](actions/list-public-assets.md) | `GET /public/assets` | [docs](https://ridb.recreation.gov/shared/swagger/ridb.yaml) |
| [List Public Organizations](actions/list-public-organizations.md) | `GET /public/organizations` | [docs](https://ridb.recreation.gov/shared/swagger/ridb.yaml) |
| [List Rec Area Activities](actions/list-rec-area-activities.md) | `GET /recareas/{id}/activities` | [docs](https://ridb.recreation.gov/shared/swagger/ridb.yaml) |
| [List Rec Area Addresses](actions/list-rec-area-addresses.md) | `GET /recareas/{id}/recareaaddresses` | [docs](https://ridb.recreation.gov/shared/swagger/ridb.yaml) |
| [List Rec Area Events](actions/list-rec-area-events.md) | `GET /recareas/{id}/events` | [docs](https://ridb.recreation.gov/shared/swagger/ridb.yaml) |
| [Update Facility](actions/update-facility.md) | `PUT /facilities/{id}` | [docs](https://ridb.recreation.gov/shared/swagger/dataSteward.yaml) |
| [Update Facility Activity](actions/update-facility-activity.md) | `PUT /facilities/{id}/activities/{activityId}` | [docs](https://ridb.recreation.gov/shared/swagger/dataSteward.yaml) |
| [Update Facility Address](actions/update-facility-address.md) | `PUT /facilities/{id}/facilityaddresses/{addressId}` | [docs](https://ridb.recreation.gov/shared/swagger/dataSteward.yaml) |
| [Update Rec Area](actions/update-rec-area.md) | `PUT /recareas/{id}` | [docs](https://ridb.recreation.gov/shared/swagger/dataSteward.yaml) |
| [Update Rec Area Activity](actions/update-rec-area-activity.md) | `PUT /recareas/{id}/activities/{activityId}` | [docs](https://ridb.recreation.gov/shared/swagger/dataSteward.yaml) |
| [Update Rec Area Address](actions/update-rec-area-address.md) | `PUT /recareas/{id}/recareaaddresses/{addressId}` | [docs](https://ridb.recreation.gov/shared/swagger/dataSteward.yaml) |
| [Update Rec Area Event](actions/update-rec-area-event.md) | `PUT /recareas/{id}/events/{eventId}` | [docs](https://ridb.recreation.gov/shared/swagger/dataSteward.yaml) |
