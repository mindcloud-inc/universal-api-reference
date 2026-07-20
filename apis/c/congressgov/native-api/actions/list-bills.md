# List Bills with Congress.gov

Retrieves bills from Congress.gov.

## Endpoint

- **Method:** `GET`
- **Path:** `/bill`
- **Base URL:** `https://api.congress.gov/v3`
- **Official documentation:** [List Bills](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/BillEndpoint.md)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fromDateTime` | query | `date` | no | Starting timestamp to filter by update date. Use YYYY-MM-DDT00:00:00Z. |
| `toDateTime` | query | `date` | no | Ending timestamp to filter by update date. Use YYYY-MM-DDT00:00:00Z. |
