# Add Debug Metadata with Appzi

Generates Appzi debug metadata settings.

## Endpoint

- **Method:** `GET`
- **Path:** `https://docs.appzi.io/integration/add-data/`
- **Base URL:** `https://api.appzi.io`
- **Official documentation:** [Add Debug Metadata](https://docs.appzi.io/integration/add-data/#debug-issues)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appVersion` | query | `string` | no | Optional application version value to include in the debug payload. |
| `environment` | query | `string` | no | Optional environment label to include in the debug payload. |
| `browserFeatures` | query | `string` | no | Optional browser capability list to include in the debug payload. |
