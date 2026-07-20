# Prepare CSP-Compatible Appzi Install with Appzi

Retrieves a CSP-safe installation plan from Appzi.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/probe/:portalToken`
- **Base URL:** `https://api.appzi.io`
- **Official documentation:** [Prepare CSP-Compatible Appzi Install](https://docs.appzi.io/configuration/csp/#implementation-steps)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `portalToken` | path | `string` | yes | Portal token path segment used only to validate runtime against the existing Appzi probe surface. |
