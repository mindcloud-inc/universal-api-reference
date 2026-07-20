# Update Ruleset Actions with Pinghome

Updates existing ruleset actions in Pinghome.

## Endpoint

- **Method:** `PUT`
- **Path:** `/incident-cmd/v1/ruleset/:id/actions`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [Update Ruleset Actions](https://docs.pinghome.io/incident-management/ruleset-management-and-event-handling/update-ruleset-actions/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `actions` | body | `string` | no | The updated actions array for the ruleset. |
| `id` | path | `string` | no | The ruleset ID to update. |
