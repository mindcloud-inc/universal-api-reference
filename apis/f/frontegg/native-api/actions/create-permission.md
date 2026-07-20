# Create Permission with Frontegg

Creates a new permission in Frontegg.

## Endpoint

- **Method:** `POST`
- **Path:** `/identity/resources/permissions/v1`
- **Base URL:** `https://api.frontegg.com`
- **Official documentation:** [Create Permission](https://developers.frontegg.com/ciam/api/identity/permissions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | body | `string` | yes | Unique permission key. |
| `name` | body | `string` | yes | Permission display name. |
| `description` | body | `string` | no | Permission description. |
| `categoryId` | body | `string` | no | Permission category ID. |
| `assignmentType` | body | `list` | no | Permission assignment classification. |
