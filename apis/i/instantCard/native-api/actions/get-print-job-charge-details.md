# Get Print Job Charge Details with InstantCard

Retrieves submitted print job charge details from InstantCard.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/organizations/:organizationId/print_jobs/:id/charge_details`
- **Base URL:** `https://core.instantcard.net`
- **Official documentation:** [Get Print Job Charge Details](https://instantcard.net/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `number` | yes | Organization ID from your InstantCard account. |
| `id` | path | `number` | yes | ID of the print job to inspect. |
