# Get Role with Agilite

Retrieves responsible users from Agilite by role and conditional level.

## Endpoint

- **Method:** `POST`
- **Path:** `/roles/getRole`
- **Base URL:** `https://api.agilite.io`
- **Official documentation:** [Get Role](https://docs.agilite.io/reference/getrole)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `role-names` | query | `string` | yes | Role name(s) to query, separated by commas when using multiple roles. |
| `conditional-levels` | query | `string` | no | Optional conditional levels for role lookup. |
