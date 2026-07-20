# List Amendment Actions with Congress.gov

Retrieves actions for an amendment from Congress.gov.

## Endpoint

- **Method:** `GET`
- **Path:** `/amendment/:congress/:amendmentType/:amendmentNumber/actions`
- **Base URL:** `https://api.congress.gov/v3`
- **Official documentation:** [List Amendment Actions](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/AmendmentEndpoint.md)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `congress` | path | `number` | yes | The congress number. For example, 118. |
| `amendmentType` | path | `string` | yes | The amendment type. Values include hamdt, samdt, or suamdt. |
| `amendmentNumber` | path | `number` | yes | The amendment's assigned number. For example, 2137. |
