# Update Company with Aspire

Updates an existing company in your Aspire account.

## Endpoint

- **Method:** `PUT`
- **Path:** `Companies`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Update Company](https://cloud-api.youraspire.com/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyID` | body | `list<number>` | yes | — |
| `companyName` | body | `string` | yes | Minimum Length: 1 |
| `deniedTimeEmail` | body | `string` | no | — |
| `active` | body | `boolean` | no | — |
