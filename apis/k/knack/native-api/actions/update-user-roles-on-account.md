# Update User Roles On Account with Knack

## Endpoint

- **Method:** `PUT`
- **Path:** `/objects/:object_key/records/:record_id`
- **Base URL:** `https://api.knack.com/v1`
- **Official documentation:** [Update User Roles On Account](https://docs.knack.com/v3/docs/managing-user-records)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `object_key` | path | `string` | yes | User object key, such as object_1. |
| `record_id` | path | `string` | yes | User account record ID to update. |
| `userRolesFieldKey` | body | `string` | yes | Target Knack user roles field key, such as field_5. |
| `userRoleProfileKeys[]` | body | `array<string>` | yes | One or more Knack profile IDs to assign, such as profile_4. |
