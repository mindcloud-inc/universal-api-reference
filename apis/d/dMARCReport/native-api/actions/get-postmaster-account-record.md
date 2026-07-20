# Get Postmaster Account Record with DMARC Report

Retrieves a postmaster account record from DMARC Report.

## Endpoint

- **Method:** `GET`
- **Path:** `/postmaster_account_records/:id.json`
- **Base URL:** `https://api.dmarcreport.com/v2`
- **Official documentation:** [Get Postmaster Account Record](https://docs.dmarcreport.com/api/2.0.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Postmaster account record identifier from the endpoint path. |
| `email` | query | `string` | yes | Email address of the connected Postmaster account. |
| `item` | query | `string` | yes | Domain for which Postmaster data is needed. |
