# Get Law with Congress.gov

Retrieves a law from Congress.gov.

## Endpoint

- **Method:** `GET`
- **Path:** `/law/:congress/:lawType/:lawNumber`
- **Base URL:** `https://api.congress.gov/v3`
- **Official documentation:** [Get Law](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/BillEndpoint.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `congress` | path | `number` | yes | The congress number. For example, 118. |
| `lawType` | path | `string` | yes | The law type. Values are pub or priv. |
| `lawNumber` | path | `number` | yes | The law number. |
