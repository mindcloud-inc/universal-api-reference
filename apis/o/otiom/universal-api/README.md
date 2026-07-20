# <img src="https://images.mindcloud.co/apps/icons/otiom_1776452140866.png" alt="Otiom logo" width="28" height="28"> Otiom: Universal API

Otiom provides access to patients, alerts, geofences, devices, and related safety data for Otiom care workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/otiom/latest
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://otiom.com
- **Vendor API docs:** https://api.otiom.com/swagger/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Patients](actions/list-patients.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/otiom/latest/actions/list-patients?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### Alarm

| Action | Method | Description |
| --- | --- | --- |
| [List Active Alarms](actions/list-active-alarms.md) | GET | Retrieves active alarms from Otiom. |
| [List Alarms](actions/list-alarms.md) | GET | Retrieves alarms from Otiom. |

### Alert

| Action | Method | Description |
| --- | --- | --- |
| [Get Active Alerts](actions/get-active-alerts.md) | GET | Retrieves active alerts from Otiom. |

### Beacon

| Action | Method | Description |
| --- | --- | --- |
| [List Beacons](actions/list-beacons.md) | GET | Retrieves beacons from Otiom. |

### Companion

| Action | Method | Description |
| --- | --- | --- |
| [List Companions](actions/list-companions.md) | GET | Retrieves companions from Otiom. |

### Geofence

| Action | Method | Description |
| --- | --- | --- |
| [Create Geofence](actions/create-geofence.md) | POST | Creates a new geofence in Otiom. |
| [Get Geofence](actions/get-geofence.md) | GET | Retrieves a geofence from Otiom. |
| [List Geofences](actions/list-geofences.md) | GET | Retrieves geofences from Otiom. |

### Helper

| Action | Method | Description |
| --- | --- | --- |
| [List Helpers](actions/list-helpers.md) | GET | Retrieves helpers from Otiom. |

### Patient

| Action | Method | Description |
| --- | --- | --- |
| [Create Patient](actions/create-patient.md) | POST | Creates a new patient in Otiom. |
| [Get Patient](actions/get-patient.md) | GET | Retrieves a patient from Otiom. |
| [List Patients](actions/list-patients.md) | GET | Retrieves patients from Otiom. |

### Patient Alarm Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Patient Alarm Status](actions/get-patient-alarm-status.md) | GET | Retrieves a patient's alarm status from Otiom. |

### Patient Helper

| Action | Method | Description |
| --- | --- | --- |
| [List Patient Helpers](actions/list-patient-helpers.md) | GET | Retrieves helpers for a patient from Otiom. |

### Patient Homebase

| Action | Method | Description |
| --- | --- | --- |
| [Get Patient Homebase](actions/get-patient-homebase.md) | GET | Retrieves a patient's homebase from Otiom. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from Otiom. |

### Track

| Action | Method | Description |
| --- | --- | --- |
| [List Tracks](actions/list-tracks.md) | GET | Retrieves tracks from Otiom. |

