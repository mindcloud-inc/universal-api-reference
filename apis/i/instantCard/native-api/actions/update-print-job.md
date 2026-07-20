# Update Print Job with InstantCard

Updates an existing print job in InstantCard.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v2/organizations/:organizationId/print_jobs/:id`
- **Base URL:** `https://core.instantcard.net`
- **Official documentation:** [Update Print Job](https://instantcard.net/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `number` | yes | Organization ID from your InstantCard account. |
| `id` | path | `number` | yes | ID of the print job to update. |
| `print_job[number_of_copies]` | query | `number` | no | Number of copies to print for each card in the print job. |
| `print_job[shipping_provider_id]` | query | `number` | no | Shipping provider ID to use for the print job. |
| `print_job[address_id]` | query | `number` | no | Saved address ID to use for shipping. |
