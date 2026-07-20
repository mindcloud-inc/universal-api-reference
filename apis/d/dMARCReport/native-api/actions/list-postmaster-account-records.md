# List Postmaster Account Records with DMARC Report

Retrieves postmaster account records from DMARC Report.

## Endpoint

- **Method:** `GET`
- **Path:** `/postmaster_account_records.json`
- **Base URL:** `https://api.dmarcreport.com/v2`
- **Official documentation:** [List Postmaster Account Records](https://docs.dmarcreport.com/api/2.0.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | yes | Email address of the Postmaster account to retrieve cumulative domain data for. |
