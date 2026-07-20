# Batch Delete Users with Didit

Deletes multiple users from Didit.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/delete/`
- **Base URL:** `https://verification.didit.me/v3`
- **Official documentation:** [Batch Delete Users](https://docs.didit.me/management-api/users/delete)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `vendor_data_list` | body | `list<string>` | yes |
