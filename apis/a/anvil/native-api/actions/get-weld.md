# Get Weld with Anvil

Retrieves a single weld from Anvil.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://graphql.useanvil.com`
- **Official documentation:** [Get Weld](https://www.useanvil.com/docs/api/graphql/reference/#query-weld)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.eid` | body | `string` | no | Provide EID for Get Weld. |
| `variables.slug` | body | `string` | no | Provide Slug for Get Weld. |
| `variables.organizationSlug` | body | `string` | no | Provide Organization Slug for Get Weld. |
| `variables.versionNumber` | body | `number` | no | Provide Version Number for Get Weld. |
