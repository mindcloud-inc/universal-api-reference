# Enrich Company with Captain Data

Retrieves detailed company data from Captain Data by LinkedIn URL.

## Endpoint

- **Method:** `GET`
- **Path:** `/companies/enrich`
- **Base URL:** `https://api.captaindata.com/v1`
- **Official documentation:** [Enrich Company](https://docs.captaindata.com/v1/api/companies/enrich)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `li_company_url` | query | `string` | yes | LinkedIn company URL to enrich. |
