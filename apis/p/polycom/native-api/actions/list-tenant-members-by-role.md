# List Tenant Members By Role with Polycom

Lists tenant members in Poly Lens for a selected role.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.silica-prod01.io.lens.poly.com`
- **Official documentation:** [List Tenant Members By Role](https://api.lens.poly.com/docs/graphql/Example%20Queries/platform-management-queries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | GraphQL document for the tenant-member search. |
| `variables.params.grants[0].resourceId` | body | `string` | yes | The tenant to search for users. |
| `variables.params.grants[0].roles` | body | `string` | yes | Supported Poly Lens roles include admin, it-admin, user, and device_user. |
