# Start Validation with Rossum

Starts validation for an annotation in Rossum.

## Endpoint

- **Method:** `POST`
- **Path:** `/annotations/:annotationID/start`
- **Base URL:** `https://mindcloud.rossum.app/api/v1`
- **Official documentation:** [Start Validation](https://rossum.app/api/docs/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `annotationID` | path | `number` | yes | Rossum annotation ID. |
| `statuses[]` | body | `array<string>` | no | Optional allowed statuses when starting validation. |
