# Otiom: Native API Reference

A consolidated summary of Otiom's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://api.otiom.com/swagger/
- **OpenAPI specification:** https://api.otiom.com/schema/
- **API base URL:** `https://api.otiom.com`

## Authentication

### API Token

Token-based authentication using the Authorization header with the provider-required Token prefix.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.otiom.com/swagger/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Geofence](actions/create-geofence.md) | `POST /api/geofences/` | [docs](https://api.otiom.com/swagger/) |
| [Create Patient](actions/create-patient.md) | `POST /api/patients/` | [docs](https://api.otiom.com/swagger/) |
| [Get Active Alerts](actions/get-active-alerts.md) | `GET /api/alerts/active` | [docs](https://api.otiom.com/swagger/) |
| [Get Geofence](actions/get-geofence.md) | `GET /api/geofences/:id/` | [docs](https://api.otiom.com/swagger/) |
| [Get Patient](actions/get-patient.md) | `GET /api/patients/:id/` | [docs](https://api.otiom.com/swagger/) |
| [Get Patient Alarm Status](actions/get-patient-alarm-status.md) | `GET /api/patients/:id/has_alarm/` | [docs](https://api.otiom.com/swagger/) |
| [Get Patient Homebase](actions/get-patient-homebase.md) | `GET /api/patients/:patientid/homebase/` | [docs](https://api.otiom.com/swagger/) |
| [List Active Alarms](actions/list-active-alarms.md) | `GET /api/alarms/active/` | [docs](https://api.otiom.com/swagger/) |
| [List Alarms](actions/list-alarms.md) | `GET /api/alarms/` | [docs](https://api.otiom.com/swagger/) |
| [List Beacons](actions/list-beacons.md) | `GET /api/beacons/` | [docs](https://api.otiom.com/swagger/) |
| [List Companions](actions/list-companions.md) | `GET /api/companions/` | [docs](https://api.otiom.com/swagger/) |
| [List Geofences](actions/list-geofences.md) | `GET /api/geofences/` | [docs](https://api.otiom.com/swagger/) |
| [List Helpers](actions/list-helpers.md) | `GET /api/helpers/` | [docs](https://api.otiom.com/swagger/) |
| [List Patient Helpers](actions/list-patient-helpers.md) | `GET /api/patients/:patientid/helpers/` | [docs](https://api.otiom.com/swagger/) |
| [List Patients](actions/list-patients.md) | `GET /api/patients/` | [docs](https://api.otiom.com/swagger/) |
| [List Tags](actions/list-tags.md) | `GET /api/tag/` | [docs](https://api.otiom.com/swagger/) |
| [List Tracks](actions/list-tracks.md) | `GET /api/track/` | [docs](https://api.otiom.com/swagger/) |
