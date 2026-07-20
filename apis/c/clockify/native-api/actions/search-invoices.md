# Search Invoices with Clockify

Finds invoices in Clockify by filters.

## Endpoint

- **Method:** `POST`
- **Path:** `workspaces/:workspaceId/invoices/info`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Search Invoices](https://docs.developer.clockify.me/#tag/Invoice/operation/getInvoicesInfo)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes | — |
| `clients` | body | `object` | no | — |
| `companies` | body | `object` | no | — |
| `exactAmount` | body | `number` | no | — |
| `exactBalance` | body | `number` | no | — |
| `greaterThanAmount` | body | `number` | no | — |
| `greaterThanBalance` | body | `number` | no | — |
| `invoiceNumber` | body | `string` | no | — |
| `issueDate` | body | `object` | no | — |
| `lessThanAmount` | body | `number` | no | — |
| `lessThanBalance` | body | `number` | no | — |
| `page` | body | `number` | no | — |
| `pageSize` | body | `number` | no | — |
| `sortColumn` | body | `list<string>` | no | Accepted values: `AMOUNT`, `BALANCE`, `CLIENT`, `DUE_ON`, `ID`, `ISSUE_DATE`. |
| `sortOrder` | body | `list<string>` | no | Accepted values: `ASCENDING`, `DESCENDING`. |
| `statuses[]` | body | `array<string>` | no | — |
| `strictSearch` | body | `boolean` | no | — |
| `clients.contains` | body | `string` | no | — |
| `clients.ids[]` | body | `array<string>` | no | — |
| `clients.status` | body | `string` | no | — |
| `companies.contains` | body | `string` | no | — |
| `companies.ids[]` | body | `array<string>` | no | — |
| `issueDate.issue-date-end` | body | `string` | no | — |
| `issueDate.issue-date-start` | body | `string` | no | — |
