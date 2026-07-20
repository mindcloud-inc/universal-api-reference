# Get MTA-STS Report with DMARC Report

Retrieves an MTA-STS report from DMARC Report.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/domains/:domainId/mta_sts_reports/:id.json`
- **Base URL:** `https://api.dmarcreport.com/v2`
- **Official documentation:** [Get MTA-STS Report](https://docs.dmarcreport.com/api/2.0.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | DMARC Report account identifier from the endpoint path. |
| `domainId` | path | `string` | yes | Domain identifier from the endpoint path. |
| `id` | path | `string` | yes | MTA-STS report identifier from the endpoint path. |
