# Create Submission with Anvil

Creates a new submission in Anvil.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://graphql.useanvil.com`
- **Official documentation:** [Create Submission](https://www.useanvil.com/docs/api/graphql/reference/#mutation-createSubmission)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.forgeEid` | body | `string` | yes | Provide Forge EID for Create Submission. |
| `variables.weldDataEid` | body | `string` | yes | Provide Weld Data EID for Create Submission. |
