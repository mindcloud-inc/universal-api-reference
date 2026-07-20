# List Ruleset Actions with Pinghome

Retrieves ruleset actions from Pinghome.

## Endpoint

- **Method:** `GET`
- **Path:** `/incident-query/v1/ruleset/:id/actions`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [List Ruleset Actions](https://docs.pinghome.io/incident-management/ruleset-management-and-event-handling/get-ruleset-actions/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ruleset ID. |
