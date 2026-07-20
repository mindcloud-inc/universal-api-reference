# Update Lead Status with LaGrowthMachine

Updates a lead's status in LaGrowthMachine.

## Endpoint

- **Method:** `POST`
- **Path:** `/leads/status`
- **Base URL:** `https://apiv2.lagrowthmachine.com/flow`
- **Official documentation:** [Update Lead Status](https://documenter.getpostman.com/view/2071164/TVCmSkH2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign[]` | body | `array<string>` | yes | Campaign name list to scope the status update to. |
| `from` | body | `string` | no | Optional status update source. |
| `memberEmail` | body | `string` | no | Optional member email used with the `from` field. |
| `persoEmail` | body | `string` | no | Lead personal email used to identify the lead. |
| `proEmail` | body | `string` | no | Lead professional email used to identify the lead. |
| `status` | body | `string` | yes | New lead status value. |
