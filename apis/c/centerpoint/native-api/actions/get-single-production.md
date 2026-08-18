# Get Single Production with Centerpoint

## Endpoint

- **Method:** `GET`
- **Path:** `productions/:PRODUCTION_ID?include=availableTransitions,availableTransitions.fromStage,availableTransitions.toStage`
- **Base URL:** `https://api.centerpointconnect.io/centerpoint/`

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `PRODUCTION_ID` | path | `string` | yes |
