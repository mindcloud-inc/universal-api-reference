# Capture Canvas WebGL Content with Appzi

Retrieves a canvas and WebGL capture snippet from Appzi.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/probe/:portalToken`
- **Base URL:** `https://api.appzi.io`
- **Official documentation:** [Capture Canvas WebGL Content](https://docs.appzi.io/configuration/screenshots/#canvaswebgl-capture)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `portalToken` | path | `string` | yes | Portal token path segment used only to validate runtime against the existing Appzi probe surface. |
