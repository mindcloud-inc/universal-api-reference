# Get All Resource Features with Mews

Retrieves resource features from Mews.

## Endpoint

- **Method:** `POST`
- **Path:** `/resourceFeatures/getAll`
- **Base URL:** `{platformAddress}/api/connector/v1`
- **Official documentation:** [Get All Resource Features](https://github.com/MewsSystems/gitbook-connector-api/blob/master/operations/resourcefeatures.md#get-all-resource-features)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ServiceIds[]` | body | `array<string>` | yes | Service identifiers whose resource features should be returned. |
