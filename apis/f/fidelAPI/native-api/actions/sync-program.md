# Sync Program with Fidel API

Syncs an existing program in Fidel API.

## Endpoint

- **Method:** `PUT`
- **Path:** `/programs/:programId`
- **Base URL:** `https://api.fidel.uk/v1`
- **Official documentation:** [Sync Program](https://reference.fidel.uk/reference/sync-program)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `programId` | path | `string` | yes | ProgramId to be synced. This only works with live programs, so make sure the programId you're using is from a live program. |
