# List Laws By Congress with Congress.gov

Retrieves laws from a specific Congress in Congress.gov.

## Endpoint

- **Method:** `GET`
- **Path:** `/law/:congress`
- **Base URL:** `https://api.congress.gov/v3`
- **Official documentation:** [List Laws By Congress](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/BillEndpoint.md)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `congress` | path | `number` | yes | The congress number. For example, 118. |
