# Get Company Holiday with BambooHR

Retrieves company holiday from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/holidays/:id`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Company Holiday](https://documentation.bamboohr.com/reference/get-company-holiday)

## Requirements

- **OAuth scopes:** `holidays`
- **scope:** `holidays` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The company holiday ID. |
