# List Tenant Admins with Polycom

Lists admin users for a selected Poly Lens tenant.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.silica-prod01.io.lens.poly.com`
- **Official documentation:** [List Tenant Admins](https://api.lens.poly.com/docs/graphql/Example%20Queries/platform-management-queries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Prefilled GraphQL document for the tenant-admins query. Keep visible due safety restrictions on hiding new privileged defaults. |
| `variables.params.grants[0].resourceId` | body | `string` | yes | The tenant to search for administrator users. |
