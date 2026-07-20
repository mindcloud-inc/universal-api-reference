# Create Company with Aspire

Add a new company.

## Endpoint

- **Method:** `POST`
- **Path:** `Companies`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Create Company](https://cloud-api.youraspire.com/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyName` | body | `string` | yes | Minimum Length: 1 |
| `deniedTimeEmail` | body | `string` | no | — |
| `active` | body | `boolean` | no | — |
