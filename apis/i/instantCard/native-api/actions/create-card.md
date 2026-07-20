# Create Card with InstantCard

Creates a new draft card in InstantCard.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/organizations/:organizationId/cards`
- **Base URL:** `https://core.instantcard.net`
- **Official documentation:** [Create Card](https://instantcard.net/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | Organization ID from your InstantCard account. |
| `card.card_template_id` | body | `number` | yes | Template ID to use for the new card. |
| `card.data[]` | body | `array<object>` | yes | Array of card field objects, including text and image values. |
