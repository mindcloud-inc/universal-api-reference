# List Laws By Congress And Type with Congress.gov

Retrieves laws by Congress and law type in Congress.gov.

## Endpoint

- **Method:** `GET`
- **Path:** `/law/:congress/:lawType`
- **Base URL:** `https://api.congress.gov/v3`
- **Official documentation:** [List Laws By Congress And Type](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/BillEndpoint.md)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `congress` | path | `number` | yes | The congress number. For example, 118. |
| `lawType` | path | `string` | yes | The law type. Values are pub or priv. |
