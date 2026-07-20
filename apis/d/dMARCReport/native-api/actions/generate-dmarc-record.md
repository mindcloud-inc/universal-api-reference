# Generate DMARC Record with DMARC Report

Generates a DMARC record for a domain in DMARC Report.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountId/domains/:domainId/generate_dmarc_record.json`
- **Base URL:** `https://api.dmarcreport.com/v2`
- **Official documentation:** [Generate DMARC Record](https://docs.dmarcreport.com/api/2.0.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | DMARC Report account identifier from the endpoint path. |
| `domainId` | path | `string` | yes | Domain identifier from the endpoint path. |
| `p` | body | `string` | yes | DMARC policy to generate in the record. |
| `sp` | body | `string` | no | Optional DMARC policy for subdomains. |
| `pct` | body | `number` | no | Percentage of messages to which the DMARC policy applies. |
| `adkim` | body | `string` | no | DKIM alignment mode: relaxed or strict. |
| `aspf` | body | `string` | no | SPF alignment mode: relaxed or strict. |
| `fo` | body | `string` | no | DMARC forensic reporting options, such as 0, 1, d, s, or a colon-separated combination. |
| `additional_rua_emails[]` | body | `array<string>` | no | Additional email addresses for aggregate reports. Send multiple values as a array. |
| `additional_ruf_emails[]` | body | `array<string>` | no | Additional email addresses for forensic reports. Send multiple values as a array. |
| `t` | body | `string` | no | DMARCbis test mode value: y or n. |
| `psd` | body | `string` | no | DMARCbis public suffix domain value: y, n, or u. |
| `np` | body | `string` | no | DMARCbis policy for non-existent subdomains. |
| `publish` | body | `boolean` | no | Whether to publish this generated record to hosted DMARC. |
