# Create Stage0 Entry with Inistate

Creates a new Stage0 entry in Inistate.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/activity`
- **Base URL:** `https://api.inistate.com`
- **Official documentation:** [Create Stage0 Entry](https://app.swaggerhub.com/apis-docs/Inistate/InistateAPI/1.0.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `payload` | body | `object` | no | Optional field payload keyed by provider field names. An empty object creates the default untitled entry shape verified in this run. |
