# Count Tenant Admins with Polycom

Counts admin users in a selected Poly Lens tenant.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.silica-prod01.io.lens.poly.com`
- **Official documentation:** [Count Tenant Admins](https://api.lens.poly.com/docs/graphql/Example%20Queries/platform-management-queries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.params.grants[0].resourceId` | body | `string` | yes | The Poly Lens tenant ID to scope the admin user count. |
