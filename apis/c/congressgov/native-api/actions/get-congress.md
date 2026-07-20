# Get Congress with Congress.gov

Retrieves a Congress session from Congress.gov.

## Endpoint

- **Method:** `GET`
- **Path:** `/congress/:congress`
- **Base URL:** `https://api.congress.gov/v3`
- **Official documentation:** [Get Congress](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/CongressEndpoint.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `congress` | path | `number` | yes | The congress number. For example, 118. |
