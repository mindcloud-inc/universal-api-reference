# Cancel Gift with Loop & Tie

Cancels an unredeemed gift in Loop & Tie.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/teams/:teamId/gifts/:giftId`
- **Base URL:** `https://api.loopandtie.com/v1`
- **Official documentation:** [Cancel Gift](https://docs.loopandtie.com/reference/teamsteam_idgiftsid-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `giftId` | path | `string` | no | The Loop & Tie gift ID. |
| `teamId` | path | `string` | no | The Loop & Tie team ID. |
