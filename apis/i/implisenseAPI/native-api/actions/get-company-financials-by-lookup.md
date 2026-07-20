# Get Company Financials By Lookup with Implisense

Finds company financials in Implisense API by lookup.

## Endpoint

- **Method:** `POST`
- **Path:** `/companies/financials`
- **Base URL:** `https://german-company-data.p.rapidapi.com`
- **Official documentation:** [Get Company Financials By Lookup](https://docs.implisense.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Known company text, for example a company name and city. |
| `name` | body | `string` | no | Official company name. |
| `city` | body | `string` | no | City of the company headquarters. |
| `active` | body | `boolean` | no | Return only companies that are still active. |
