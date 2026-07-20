# Add Custom Feedback Data with Appzi

Generates Appzi custom feedback data settings.

## Endpoint

- **Method:** `GET`
- **Path:** `https://docs.appzi.io/integration/add-data/`
- **Base URL:** `https://api.appzi.io`
- **Official documentation:** [Add Custom Feedback Data](https://docs.appzi.io/integration/add-data/#adding-additional-data-to-feedback)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataJson` | query | `string` | no | Optional JSON object to merge into the Appzi feedback data payload. |
