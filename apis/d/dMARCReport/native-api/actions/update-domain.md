# Update Domain with DMARC Report

Updates an existing domain in DMARC Report.

## Endpoint

- **Method:** `PUT`
- **Path:** `/accounts/:accountId/domains/:id.json`
- **Base URL:** `https://api.dmarcreport.com/v2`
- **Official documentation:** [Update Domain](https://docs.dmarcreport.com/api/2.0.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | DMARC Report account identifier from the endpoint path. |
| `id` | path | `string` | yes | Domain identifier from the endpoint path. |
| `domain` | body | `object` | yes | Domain update hash. Supported keys include rua_report, ruf_report, mta_sts_report, hosted_dmarc, hosted_dmarc_config, and hosted_mta_sts. |
