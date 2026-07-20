# Delete Domain with DMARC Report

Deletes a domain from DMARC Report.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/accounts/:accountId/domains/:id.json`
- **Base URL:** `https://api.dmarcreport.com/v2`
- **Official documentation:** [Delete Domain](https://docs.dmarcreport.com/api/2.0.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | DMARC Report account identifier from the endpoint path. |
| `id` | path | `string` | yes | Domain identifier from the endpoint path. |
