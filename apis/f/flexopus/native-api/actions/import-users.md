# Import Users with Flexopus

Imports users into Flexopus from a file.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/import`
- **Base URL:** `{tenantBaseUrl}/api/v1`
- **Official documentation:** [Import Users](https://flexopus.com/api/docs/#endpoints-POSTapi-v1-users-import)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Accepted file formats: csv, txt, ods, xls, xlsx. |
| `update` | body | `boolean` | no | Whether existing users should be updated. |
| `restore` | body | `boolean` | no | Whether deactivated users present in the list should be re-activated. |
| `deactivate` | body | `boolean` | no | Whether users not present in the list should be deactivated. |
| `key_column` | body | `list<string>` | no | Column used to identify existing users during import. Accepted values: `email`, `id`, `upn`. |
| `dry_run` | body | `boolean` | no | Simulate the import without making modifications. |
