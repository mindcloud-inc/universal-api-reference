# Exclude Elements From Screenshots with Appzi

Retrieves a screenshot exclusion snippet from Appzi.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/probe/:portalToken`
- **Base URL:** `https://api.appzi.io`
- **Official documentation:** [Exclude Elements From Screenshots](https://docs.appzi.io/configuration/screenshots/#exclude-elements)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `portalToken` | path | `string` | yes | Portal token path segment used only to validate runtime against the existing Appzi probe surface. |
