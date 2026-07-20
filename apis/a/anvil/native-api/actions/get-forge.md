# Get Forge with Anvil

Retrieves a single forge from Anvil.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://graphql.useanvil.com`
- **Official documentation:** [Get Forge](https://www.useanvil.com/docs/api/graphql/reference/#query-forge)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.organizationSlug` | body | `string` | no | Provide Organization Slug for Get Forge. |
| `variables.eidOrSlug` | body | `string` | no | Provide EID Or Slug for Get Forge. |
| `variables.eid` | body | `string` | no | Provide EID for Get Forge. |
| `variables.weldDataEid` | body | `string` | no | Provide Weld Data EID for Get Forge. |
| `variables.submissionEid` | body | `string` | no | Provide Submission EID for Get Forge. |
| `variables.versionNumber` | body | `number` | no | Provide Version Number for Get Forge. |
