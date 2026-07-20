# Add Cards To Print Job with InstantCard

Updates an existing print job in InstantCard by adding cards.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/organizations/:organizationId/print_jobs/:id/add_cards`
- **Base URL:** `https://core.instantcard.net`
- **Official documentation:** [Add Cards To Print Job](https://instantcard.net/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `number` | yes | Organization ID from your InstantCard account. |
| `id` | path | `number` | yes | ID of the print job to update. |
| `print_job[card_ids]` | query | `string` | yes | Array string of card IDs to add, exactly as InstantCard expects, for example [3096409,3145927]. |
