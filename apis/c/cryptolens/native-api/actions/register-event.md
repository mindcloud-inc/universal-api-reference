# Register Event with Cryptolens

Creates an analytics event in Cryptolens.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/ai/RegisterEvent`
- **Base URL:** `https://api.cryptolens.io`
- **Official documentation:** [Register Event](https://app.cryptolens.io/docs/api/v3/RegisterEvent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Currency` | query | `string` | no | Currency code for the event value. |
| `EventName` | query | `string` | no | Event name such as click or start. |
| `FeatureName` | query | `string` | no | Feature name associated with the event. |
| `Key` | query | `string` | no | License key string. |
| `MachineCode` | query | `string` | no | Machine code or device identifier. |
| `Metadata` | query | `string` | no | Event metadata as a JSON string. |
| `ProductId` | query | `string` | no | Product ID. Required only when Key is also supplied. |
| `v` | query | `string` | no | Method version. |
| `Value` | query | `string` | no | Integer event value; for example 2530 for 25.30. |
