# Update Lead Status with Nutshell

Updates a lead's status in Nutshell.

## Endpoint

- **Method:** `POST`
- **Path:** `/leads/:id/status`
- **Base URL:** `https://app.nutshell.com/rest`
- **Official documentation:** [Update Lead Status](https://developers.nutshell.com/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Nutshell lead ID to update. |
| `outcomeId` | body | `string` | no | The outcome ID to set for the lead. |
| `competitorMaps[]` | body | `array<string>` | no | Competitor IDs to associate when updating the lead status. Send multiple values as a array. |
