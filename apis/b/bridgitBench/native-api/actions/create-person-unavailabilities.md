# Create Person Unavailabilities with Bridgit Bench

## Endpoint

- **Method:** `POST`
- **Path:** `/rp/api/v1/accounts/:accountId/persons/:id/unavailabilities`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Create Person Unavailabilities](https://developers.gobridgit.com/reference/personunavailabilities_addunavailabilities)

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
| `payload[].description` | body | `string` | no | Maximum length: 50. |
| `payload[].startDate` | body | `date` | yes | — |
| `payload[].endDate` | body | `date` | no | — |
| `payload[].isPrivate` | body | `boolean` | yes | — |
| `payload[].rangeType` | body | `list<string>` | yes | Accepted values: `PostEmployment`, `PreEmployment`, `TimeOff`, `Unavailability`. |
