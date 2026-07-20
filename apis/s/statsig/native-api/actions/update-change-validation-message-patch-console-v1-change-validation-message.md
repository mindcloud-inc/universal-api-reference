# Update change validation message with Statsig

Updates a change validation message in Statsig.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/console/v1/change_validation/message`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Update change validation message](https://docs.statsig.com/api-reference/change-validation/update-change-validation-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reviewID` | body | `string` | yes | Request body field. |
| `message` | body | `string` | no | Request body field. |
