# List MTA-STS Failure Details with DMARC Report

Retrieves MTA-STS failure details from DMARC Report.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/domains/:domainId/mta_sts_reports/mta_failure_details.json`
- **Base URL:** `https://api.dmarcreport.com/v2`
- **Official documentation:** [List MTA-STS Failure Details](https://docs.dmarcreport.com/api/2.0.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | DMARC Report account identifier from the endpoint path. |
| `domainId` | path | `string` | yes | Domain identifier from the endpoint path. |
