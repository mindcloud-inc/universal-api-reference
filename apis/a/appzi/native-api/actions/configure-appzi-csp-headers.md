# Configure Appzi CSP Headers with Appzi

Retrieves CSP header directives from Appzi.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/probe/:portalToken`
- **Base URL:** `https://api.appzi.io`
- **Official documentation:** [Configure Appzi CSP Headers](https://docs.appzi.io/configuration/csp/#2-configure-csp-headers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `portalToken` | path | `string` | yes | Portal token path segment used only to validate runtime against the existing Appzi probe surface. |
