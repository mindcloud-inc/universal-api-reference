# Get Hosted Services with DMARC Report

Retrieves hosted service status for a domain in DMARC Report.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/domains/:domainId/hosted_services.json`
- **Base URL:** `https://api.dmarcreport.com/v2`
- **Official documentation:** [Get Hosted Services](https://docs.dmarcreport.com/api/2.0.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | DMARC Report account identifier from the endpoint path. |
| `domainId` | path | `string` | yes | Domain identifier from the endpoint path. |
