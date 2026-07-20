# Capture Specific Elements In Screenshots with Appzi

Retrieves a screenshot element-capture snippet from Appzi.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/probe/:portalToken`
- **Base URL:** `https://api.appzi.io`
- **Official documentation:** [Capture Specific Elements In Screenshots](https://docs.appzi.io/configuration/screenshots/#capture-specific-elements)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `portalToken` | path | `string` | yes | Portal token used only to validate runtime against the existing Appzi probe surface and enrich the snippet output with current survey context. |
