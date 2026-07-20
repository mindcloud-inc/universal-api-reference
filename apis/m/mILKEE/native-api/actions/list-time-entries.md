# List Time Entries with MILKEE

Retrieves time entries from MILKEE.

## Endpoint

- **Method:** `GET`
- **Path:** `/companies/:companyId/times`
- **Base URL:** `https://app.milkee.ch/api/v2`
- **Official documentation:** [List Time Entries](https://apidocs.milkee.ch/api/resources/times.html#list-time-entries)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | path | `string` | yes | The numeric MILKEE company ID used in the request path. |
