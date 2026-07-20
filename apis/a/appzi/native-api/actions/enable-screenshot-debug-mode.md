# Enable Screenshot Debug Mode with Appzi

Retrieves a screenshot debug mode snippet from Appzi.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/probe/:portalToken`
- **Base URL:** `https://api.appzi.io`
- **Official documentation:** [Enable Screenshot Debug Mode](https://docs.appzi.io/configuration/screenshots/#debug-mode)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `portalToken` | path | `string` | yes | Portal token used only to validate runtime against the existing Appzi probe surface and enrich the snippet output with current survey context. |
