# Get Catalog Holiday with BambooHR

Retrieves catalog holiday from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/holidays/catalog/:uuid`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Catalog Holiday](https://documentation.bamboohr.com/reference/get-catalog-holiday)

## Requirements

- **OAuth scopes:** `holidays`
- **scope:** `holidays` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | The catalog entry UUID. |
