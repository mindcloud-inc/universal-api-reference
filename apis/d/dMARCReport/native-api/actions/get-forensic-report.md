# Get Forensic Report with DMARC Report

Retrieves a forensic report from DMARC Report.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/domains/:domainId/forensic_reports/:id.json`
- **Base URL:** `https://api.dmarcreport.com/v2`
- **Official documentation:** [Get Forensic Report](https://docs.dmarcreport.com/api/2.0.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | DMARC Report account identifier from the endpoint path. |
| `domainId` | path | `string` | yes | Domain identifier from the endpoint path. |
| `id` | path | `string` | yes | Forensic report identifier from the endpoint path. |
