# Get Card Template Fields with InstantCard

Retrieves card template fields from InstantCard.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/organizations/:organizationId/card_templates/:id/fields`
- **Base URL:** `https://core.instantcard.net`
- **Official documentation:** [Get Card Template Fields](https://instantcard.net/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `number` | yes | Organization ID from InstantCard. |
| `id` | path | `number` | yes | Card template ID from InstantCard. |
