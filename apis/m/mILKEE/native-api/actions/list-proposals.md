# List Proposals with MILKEE

Retrieves proposals from MILKEE.

## Endpoint

- **Method:** `GET`
- **Path:** `/companies/:companyId/proposals`
- **Base URL:** `https://app.milkee.ch/api/v2`
- **Official documentation:** [List Proposals](https://apidocs.milkee.ch/api/resources/proposals.html#alle-offerten-auflisten)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | path | `string` | yes | The numeric MILKEE company ID used in the request path. |
