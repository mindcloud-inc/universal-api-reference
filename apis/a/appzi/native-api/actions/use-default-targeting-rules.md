# Use Default Targeting Rules with Appzi

Retrieves default targeting rules and a snippet from Appzi.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/probe/:portalToken`
- **Base URL:** `https://api.appzi.io`
- **Official documentation:** [Use Default Targeting Rules](https://docs.appzi.io/configuration/targeting/#default-targeting)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `portalToken` | path | `string` | yes | Portal token used only to validate runtime against the existing Appzi probe surface and enrich the snippet output with current survey context. |
