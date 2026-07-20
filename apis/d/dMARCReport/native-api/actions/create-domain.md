# Create Domain with DMARC Report

Creates a domain in a DMARC Report account.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountId/domains.json`
- **Base URL:** `https://api.dmarcreport.com/v2`
- **Official documentation:** [Create Domain](https://docs.dmarcreport.com/api/2.0.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | DMARC Report account identifier from the endpoint path. |
| `domain` | body | `object` | yes | Domain attributes hash. Include address, rua_report, and ruf_report; at least one report flag must be true. |
