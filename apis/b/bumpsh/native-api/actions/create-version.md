# Create Version with Bump.sh

Creates a new documentation version in Bump.sh.

## Endpoint

- **Method:** `POST`
- **Path:** `versions`
- **Base URL:** `https://bump.sh/api/v1`
- **Official documentation:** [Create Version](https://developers.bump.sh/operation/operation-post-versions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `branch_name` | body | `string` | no | Branch name for the new version. Defaults to the main branch if omitted. |
| `documentation` | body | `string` | yes | UUID or slug of the documentation. |
| `hub` | body | `string` | no | Hub ID or slug when auto-creating a documentation inside a hub. |
| `previous_version_id` | body | `string` | no | Existing version ID used as the previous deployed version reference. |
| `documentation_name` | body | `string` | no | Name to use when auto-creating the documentation. |
| `auto_create_documentation` | body | `boolean` | no | Create the documentation if it does not exist yet. |
| `definition` | body | `string` | yes | Serialized OpenAPI or AsyncAPI definition string. |
| `temporary` | body | `boolean` | no | Create the version as a temporary change with a 7 day TTL. |
