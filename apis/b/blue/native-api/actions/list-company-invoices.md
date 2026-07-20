# List Company Invoices with Blue

Retrieves invoices for a Blue company.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.blue.cc`
- **Official documentation:** [List Company Invoices](https://blue.cc/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.companyId` | body | `string` | yes | Blue company node ID. |
| `variables.limit` | body | `number` | no | Maximum number of invoices to return. |
