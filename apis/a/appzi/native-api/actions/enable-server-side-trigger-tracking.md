# Enable Server-Side Trigger Tracking with Appzi

Retrieves a server-side trigger tracking snippet from Appzi.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/probe/:portalToken`
- **Base URL:** `https://api.appzi.io`
- **Official documentation:** [Enable Server-Side Trigger Tracking](https://docs.appzi.io/configuration/targeting/#server-side-tracking)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `portalToken` | path | `string` | yes | Portal token used only to validate runtime against the existing Appzi probe surface and enrich the snippet output with current survey context. |
