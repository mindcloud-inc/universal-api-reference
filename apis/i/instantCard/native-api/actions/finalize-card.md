# Finalize Card with InstantCard

Updates an existing card in InstantCard by finalizing it.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v2/organizations/:organizationId/cards/:id/finalize`
- **Base URL:** `https://core.instantcard.net`
- **Official documentation:** [Finalize Card](https://instantcard.net/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `number` | yes | Organization ID from your InstantCard account. |
| `id` | path | `number` | yes | ID of the card to finalize. |
