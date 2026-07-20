# List Company Identifiers with Recommand

Retrieves company identifier records from Recommand.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/companies/:companyId/identifiers`
- **Base URL:** `https://app.recommand.eu`
- **Official documentation:** [List Company Identifiers](https://recommand.eu/en/reference/company-identifiers/list-company-identifiers)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `string` | yes | companyId parameter. |
