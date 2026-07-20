# Create Account Domain with DMARC Report

Creates a domain account in DMARC Report.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountId/domain_accounts.json`
- **Base URL:** `https://api.dmarcreport.com/v2`
- **Official documentation:** [Create Account Domain](https://docs.dmarcreport.com/api/2.0.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | DMARC Report account identifier from the endpoint path. |
| `domain_account` | body | `object` | yes | Domain account payload hash. Include account_attributes with id and domain_ids. |
