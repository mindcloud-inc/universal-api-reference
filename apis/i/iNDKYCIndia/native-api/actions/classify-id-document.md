# Classify ID Document with IN-D KYC India

Retrieves ID document classification results from IN-D KYC India.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/mw/classification`
- **Base URL:** `https://api.kyc.in-d.ai`
- **Official documentation:** [Classify ID Document](https://raw.githubusercontent.com/microsoft/PowerPlatformConnectors/dev/certified-connectors/IN-D%20KYC-India/apiDefinition.swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filename` | body | `string` | yes | Image file name. IN-D supports jpg, jpeg, and png files. |
| `payload` | body | `string` | yes | Base64-encoded image content for the ID document. |
