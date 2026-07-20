# Update Program with Fidel API

Updates an existing program in Fidel API.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/programs/:programId`
- **Base URL:** `https://api.fidel.uk/v1`
- **Official documentation:** [Update Program](https://reference.fidel.uk/reference/update-program)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `programId` | path | `string` | yes | — |
| `name` | body | `string` | no | Name for the Program. Can be 4 - 50 characters long. |
