# Get Responsible BPM Roles with Agilite

Retrieves responsible BPM roles from Agilite for a BPM stub.

## Endpoint

- **Method:** `GET`
- **Path:** `/bpm/getResponsibleRoles`
- **Base URL:** `https://api.agilite.io`
- **Official documentation:** [Get Responsible BPM Roles](https://docs.agilite.io/reference/getresponsibleroles)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `process-key` | query | `string` | yes | Agilit-e BPM process key. |
| `responsible-user` | query | `string` | no | Optional responsible user filter. |
