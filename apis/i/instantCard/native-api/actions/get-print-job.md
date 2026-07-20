# Get Print Job with InstantCard

Retrieves a print job from InstantCard by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/organizations/:organizationId/print_jobs/:id`
- **Base URL:** `https://core.instantcard.net`
- **Official documentation:** [Get Print Job](https://instantcard.net/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `number` | yes | Organization ID from your InstantCard account. |
| `id` | path | `number` | yes | ID of the print job to fetch. |
