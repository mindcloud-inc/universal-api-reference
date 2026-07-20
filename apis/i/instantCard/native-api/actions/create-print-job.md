# Create Print Job with InstantCard

Creates a new print job in InstantCard.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/organizations/:organizationId/print_jobs`
- **Base URL:** `https://core.instantcard.net`
- **Official documentation:** [Create Print Job](https://instantcard.net/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `number` | yes | Organization ID from your InstantCard account. |
| `print_job` | body | `object` | yes | Print job payload including shipping, copies, cards, and either an address_id or one-off address object. |
