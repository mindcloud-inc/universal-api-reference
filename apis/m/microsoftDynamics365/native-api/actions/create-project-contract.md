# Create Project Contract with Microsoft Dynamics 365

## Endpoint

- **Method:** `POST`
- **Path:** `ProjectContracts`
- **Base URL:** `{baseURL}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataAreaId` | body | `string` | no | — |
| `ProjectContractID` | body | `string` | yes | — |
| `Name` | body | `string` | yes | — |
| `ContractDate` | body | `date` | yes | — |
| `SalesTaxGroup` | body | `string` | no | — |
| `ContractLines` | body | `string` | no | Yes/No |
| `BankAccount` | body | `string` | no | — |
| `InvoicingName` | body | `string` | no | — |
| `LockContractSalesCurrency` | body | `string` | no | Yes/No |
| `CentralBankPurposeCode` | body | `string` | no | — |
| `SalesResponsiblePersonnelNumber` | body | `string` | no | — |
| `PriceGroup` | body | `string` | no | — |
| `NetPrice` | body | `string` | no | — |
| `PurposeText` | body | `string` | no | — |
| `InvoiceFrequency` | body | `string` | no | "CurrentMth" |
| `SalesCurrency` | body | `string` | no | — |
| `DefaultPostingLevel` | body | `string` | no | — |
| `TransactionCode` | body | `string` | no | — |
| `RetainagePercent` | body | `number` | no | — |
| `MinimumTimeIncrement` | body | `number` | no | — |
| `ServiceOnDeliveryAddress` | body | `string` | no | — |
| `CustomerRetentionTermId` | body | `string` | no | — |
| `ListCodeId` | body | `string` | no | — |
| `ProgressInvoicing` | body | `boolean` | no | — |
