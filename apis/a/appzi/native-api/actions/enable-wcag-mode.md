# Enable WCAG Mode with Appzi

Retrieves Appzi WCAG mode guidance.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/probe/:portalToken`
- **Base URL:** `https://api.appzi.io`
- **Official documentation:** [Enable WCAG Mode](https://docs.appzi.io/configuration/accessibility/#enable-wcag-mode)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `portalToken` | path | `string` | yes | Portal token path segment used only to validate runtime against the existing Appzi probe surface. |
