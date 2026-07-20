# Generate Settings Object with Appzi

Generates an Appzi settings object snippet.

## Endpoint

- **Method:** `GET`
- **Path:** `https://docs.appzi.io/installation/`
- **Base URL:** `https://api.appzi.io`
- **Official documentation:** [Generate Settings Object](https://docs.appzi.io/installation/#via-the-settings-object)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `portalToken` | query | `string` | yes | Portal token inserted into the generated Appzi settings object snippet. |
| `dataJson` | query | `string` | no | Optional JSON object rendered into window.appziSettings.data in the generated snippet. |
