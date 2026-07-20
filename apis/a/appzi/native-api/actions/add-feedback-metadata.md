# Add Feedback Metadata with Appzi

Generates Appzi feedback metadata settings.

## Endpoint

- **Method:** `GET`
- **Path:** `https://docs.appzi.io/integration/add-data/`
- **Base URL:** `https://api.appzi.io`
- **Official documentation:** [Add Feedback Metadata](https://docs.appzi.io/integration/add-data/#adding-additional-data-to-feedback)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `settingsJson` | query | `string` | no | Optional JSON object rendered into window.appziSettings before Appzi loads. |
