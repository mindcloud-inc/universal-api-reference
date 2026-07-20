# Get MID with Fidel API

Retrieves a MID from a Fidel program.

## Endpoint

- **Method:** `GET`
- **Path:** `/programs/:programId/mids/:midId`
- **Base URL:** `https://api.fidel.uk/v1`
- **Official documentation:** [Get MID](https://reference.fidel.uk/reference/get-mid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `programId` | path | `string` | yes | — |
| `midId` | path | `string` | yes | The MID ID. |
