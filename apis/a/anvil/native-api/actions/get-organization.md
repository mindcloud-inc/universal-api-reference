# Get Organization with Anvil

Retrieves a single organization from Anvil.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://graphql.useanvil.com`
- **Official documentation:** [Get Organization](https://www.useanvil.com/docs/api/graphql/reference/#query-organization)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.organizationSlug` | body | `string` | no | Provide Organization Slug for Get Organization. |
| `variables.organizationEid` | body | `string` | no | Provide Organization EID for Get Organization. |
