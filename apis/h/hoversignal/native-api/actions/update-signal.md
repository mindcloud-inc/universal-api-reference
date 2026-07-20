# Update Signal with Hoversignal

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/signals/{signalId}`
- **Base URL:** `https://app.hoversignal.com`
- **Official documentation:** [Update Signal](https://app.hoversignal.com/docs/ui/index)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | — |
| `signalId` | path | `number` | yes | Signal identifier. |
| `type` | body | `string` | no | — |
| `iconType` | body | `string` | no | — |
| `order` | body | `number` | no | — |
| `displayDuration` | body | `number` | no | — |
| `frequency` | body | `string` | no | — |
| `pageFilterType` | body | `string` | no | — |
| `deviceFilter` | body | `string` | no | — |
| `isActive` | body | `boolean` | no | — |
| `isRequired` | body | `boolean` | no | — |
| `text` | body | `string` | no | — |
| `actionText` | body | `string` | no | — |
| `linkUrl` | body | `string` | no | — |
