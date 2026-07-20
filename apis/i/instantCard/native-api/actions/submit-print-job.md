# Submit Print Job with InstantCard

Updates an existing print job in InstantCard by submitting it.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/organizations/:organizationId/print_jobs/:id/print`
- **Base URL:** `https://core.instantcard.net`
- **Official documentation:** [Submit Print Job](https://instantcard.net/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `number` | yes | Organization ID from your InstantCard account. |
| `id` | path | `number` | yes | ID of the print job to submit. |
