# Include Appzi Script Under CSP with Appzi

Retrieves Appzi CSP script inclusion guidance.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/probe/:portalToken`
- **Base URL:** `https://api.appzi.io`
- **Official documentation:** [Include Appzi Script Under CSP](https://docs.appzi.io/configuration/csp/#1-include-the-appzi-script)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `portalToken` | path | `string` | yes | Portal token path segment used only to validate runtime against the existing Appzi probe surface. |
