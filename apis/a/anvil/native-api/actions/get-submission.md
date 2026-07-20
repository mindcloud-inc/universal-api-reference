# Get Submission with Anvil

Retrieves a single submission from Anvil.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://graphql.useanvil.com`
- **Official documentation:** [Get Submission](https://www.useanvil.com/docs/api/graphql/reference/#query-submission)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.organizationSlug` | body | `string` | yes | Provide Organization Slug for Get Submission. |
| `variables.forgeEidOrSlug` | body | `string` | yes | Provide Forge EID Or Slug for Get Submission. |
| `variables.eid` | body | `string` | yes | Provide EID for Get Submission. |
| `variables.forceCreate` | body | `boolean` | no | Provide Force Create for Get Submission. |
| `variables.timezone` | body | `string` | no | Provide Timezone for Get Submission. |
