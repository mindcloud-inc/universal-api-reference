# Update Person Unavailabilities with Bridgit Bench

## Endpoint

- **Method:** `PATCH`
- **Path:** `/rp/api/v1/accounts/:accountId/persons/:id/unavailabilities`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Update Person Unavailabilities](https://developers.gobridgit.com/reference/personunavailabilities_updateunavailabilities)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `id` | path | `number` | yes | Id of the person to get unavailabilities for |
| `payload[]` | body | `array<object>` | yes | — |
| `payload[].id` | body | `number` | yes | — |
| `payload[].description` | body | `string` | no | Maximum length: 50. |
| `payload[].startDate` | body | `date` | no | — |
| `payload[].endDate` | body | `date` | no | — |
| `payload[].isPrivate` | body | `boolean` | no | — |
