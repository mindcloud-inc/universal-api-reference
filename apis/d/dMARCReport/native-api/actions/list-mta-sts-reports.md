# List MTA-STS Reports with DMARC Report

Retrieves MTA-STS reports from DMARC Report.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/domains/:domainId/mta_sts_reports.json`
- **Base URL:** `https://api.dmarcreport.com/v2`
- **Official documentation:** [List MTA-STS Reports](https://docs.dmarcreport.com/api/2.0.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | DMARC Report account identifier from the endpoint path. |
| `domainId` | path | `string` | yes | Domain identifier from the endpoint path. |
