# Get Assigned BPM Roles with Agilite

Retrieves assigned BPM roles from Agilite for a BPM record.

## Endpoint

- **Method:** `GET`
- **Path:** `/bpm/getAssignedRoles`
- **Base URL:** `https://api.agilite.io`
- **Official documentation:** [Get Assigned BPM Roles](https://docs.agilite.io/reference/getassignedroles)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `process-key` | query | `string` | no | Optional process key filter for assigned roles. |
| `bpm-record-id` | query | `string` | no | Optional BPM record ID filter for assigned roles. |
| `role-names` | query | `string` | no | Optional role name filter; separate multiple role names with commas. |
