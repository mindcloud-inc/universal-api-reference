# Get Compensation Benchmark Export with BambooHR

Retrieves compensation benchmark export from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/compensation/benchmarks/details/export`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Compensation Benchmark Export](https://documentation.bamboohr.com/reference/export-compensation-benchmark-details)

## Requirements

- **OAuth scopes:** `compensation_benchmarks`
- **scope:** `compensation_benchmarks` — Required OAuth scope documented by BambooHR.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | query | `string` | yes | ID of the company job title to export benchmark details for. |
| `locationId` | query | `string` | no | Optional job location ID to restrict the export to one location. |
