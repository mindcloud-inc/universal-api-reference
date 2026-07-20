# List Aggregate Reports with DMARC Report

Retrieves aggregate reports from DMARC Report.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/domains/:domainId/agg_reports.json`
- **Base URL:** `https://api.dmarcreport.com/v2`
- **Official documentation:** [List Aggregate Reports](https://docs.dmarcreport.com/api/2.0.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | DMARC Report account identifier from the endpoint path. |
| `domainId` | path | `string` | yes | Domain identifier from the endpoint path. |
