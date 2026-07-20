# Lookup Companies with Implisense

Finds companies in Implisense API by known attributes.

## Endpoint

- **Method:** `POST`
- **Path:** `/lookup`
- **Base URL:** `https://german-company-data.p.rapidapi.com`
- **Official documentation:** [Lookup Companies](https://docs.implisense.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Known company data to match, such as a company name or city. |
| `name` | body | `string` | no | Official company name. |
| `city` | body | `string` | no | City of the company headquarters. |
| `active` | body | `boolean` | no | Return only companies that are still active. |
| `size` | query | `number` | no | Maximum number of results to return, up to 10. |
