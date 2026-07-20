# Get Account Domain with DMARC Report

Retrieves a domain account from DMARC Report.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/domain_accounts/:id`
- **Base URL:** `https://api.dmarcreport.com/v2`
- **Official documentation:** [Get Account Domain](https://docs.dmarcreport.com/api/2.0.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | DMARC Report account identifier from the endpoint path. |
| `id` | path | `string` | yes | Account domain identifier from the endpoint path. |
