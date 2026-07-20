# Update Submission with Anvil

Updates an existing submission in Anvil.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://graphql.useanvil.com`
- **Official documentation:** [Update Submission](https://www.useanvil.com/docs/api/graphql/reference/#mutation-updateSubmission)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.eid` | body | `string` | yes | Provide EID for Update Submission. |
| `variables.isExcluded` | body | `boolean` | no | Provide Is Excluded for Update Submission. |
