# Use Client-Side Screenshot Renderer with Appzi

Retrieves Appzi client-side screenshot renderer guidance.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/probe/:portalToken`
- **Base URL:** `https://api.appzi.io`
- **Official documentation:** [Use Client-Side Screenshot Renderer](https://docs.appzi.io/configuration/screenshots/#client-side-renderer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `portalToken` | path | `string` | yes | Portal token used only to validate runtime against the existing Appzi probe surface and enrich the snippet output with current survey context. |
