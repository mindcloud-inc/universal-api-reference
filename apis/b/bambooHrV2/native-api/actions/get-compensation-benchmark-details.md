# Get Compensation Benchmark Details with BambooHR

Retrieves compensation benchmark details from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/compensation/benchmarks/details`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Compensation Benchmark Details](https://documentation.bamboohr.com/reference/get-compensation-benchmark-details)

## Requirements

- **OAuth scopes:** `compensation_benchmarks`
- **scope:** `compensation_benchmarks` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | query | `string` | yes | ID of the company job title to fetch benchmark details for. |
| `locationId` | query | `string` | no | Optional job location ID. When omitted, results aggregate across all locations for the job. |
