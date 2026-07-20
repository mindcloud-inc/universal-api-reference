# List Profile Permissions with Qntrl

Retrieves profile permissions from Qntrl.

## Endpoint

- **Method:** `GET`
- **Path:** `/[:org_id]/profile/permissions/[:profile_id]`
- **Base URL:** `https://coreapi.qntrl.com/blueprint/api`
- **Official documentation:** [List Profile Permissions](https://core.qntrl.com/apidoc.html#getProfilePermissions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `org_id` | path | `string` | no | Qntrl organization ID. |
| `profile_id` | path | `string` | no | Qntrl profile ID. |
