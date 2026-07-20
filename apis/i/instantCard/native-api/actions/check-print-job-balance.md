# Check Print Job Balance with InstantCard

Retrieves whether an InstantCard print job is covered by available funds.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/organizations/:organizationId/print_jobs/:id/check_balance`
- **Base URL:** `https://core.instantcard.net`
- **Official documentation:** [Check Print Job Balance](https://instantcard.net/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `number` | yes | Organization ID from your InstantCard account. |
| `id` | path | `number` | yes | ID of the print job to check. |
