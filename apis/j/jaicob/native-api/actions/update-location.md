# Update Location with Jaicob

## Endpoint

- **Method:** `PUT`
- **Path:** `/locations/[:id]`
- **Base URL:** `https://api.jaicob.ai`
- **Official documentation:** [Update Location](https://developers.jaicob.ai/reference/update_location)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Location identifier. |
| `addressLine1` | body | `string` | yes | — |
| `addressLine2` | body | `string` | no | — |
| `email` | body | `string` | no | — |
| `phone` | body | `string` | no | — |
| `postcode` | body | `string` | yes | — |
| `city` | body | `string` | yes | — |
| `country` | body | `string` | yes | — |
| `state` | body | `string` | yes | — |
| `isHeadQuarter` | body | `boolean` | yes | — |
| `name` | body | `string` | yes | — |
| `clientId` | body | `string` | no | — |
| `vacancyIds[]` | body | `array<string>` | no | — |
| `userIds[]` | body | `array<string>` | no | — |
