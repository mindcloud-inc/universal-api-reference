# Create Opportunity with Aspire

Updates an existing pay code in your Aspire account.

## Endpoint

- **Method:** `POST`
- **Path:** `Opportunities`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Create Opportunity](https://guide.youraspire.com/apidocs/opportunities-9)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `OpportunityName` | body | `string` | yes | — |
| `OpportunityType` | body | `list<string>` | yes | Accepted values: `Contract`, `Work Order`. |
| `OpportunityStatusID` | body | `list<number>` | no | — |
| `TemplateOpportunityID` | body | `list<number>` | no | — |
| `MasterOpportunityID` | body | `list<number>` | no | — |
| `PropertyID` | body | `list<number>` | no | — |
| `BranchID` | body | `list<number>` | no | — |
| `DivisionID` | body | `list<number>` | no | — |
| `SalesTypeID` | body | `list<number>` | no | — |
| `LeadSourceID` | body | `list<number>` | no | — |
| `SalesRepID` | body | `list<number>` | no | — |
| `OperationsMgrID` | body | `list<number>` | no | — |
| `StartDate` | body | `date` | no | — |
| `EndDate` | body | `date` | no | — |
| `AnticipatedCloseDate` | body | `date` | no | — |
| `BidDueDate` | body | `date` | no | — |
| `RenewalDate` | body | `date` | no | — |
| `InvoiceType` | body | `string` | no | — |
| `Probability` | body | `number` | no | — |
| `EstimatedDollars` | body | `number` | no | — |
| `BudgetedDollars` | body | `number` | no | — |
| `CustomerContractNum` | body | `string` | no | — |
| `CustomerPONum` | body | `string` | no | — |
| `OpportunityTags` | body | `string` | no | — |
