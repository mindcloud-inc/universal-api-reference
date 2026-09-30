# Microsoft Dynamics 365 Universal API Examples

These examples use the MindCloud API key and Microsoft Dynamics 365 connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Accounts



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftDynamics365/latest/actions/get-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftDynamics365/latest/actions/get-accounts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "@odata": {
        "context": "string",
        "etag": "string"
      },
      "ActiveRevision": "string",
      "ActualEndDate": "string",
      "ActualStartDate": "string",
      "AlertTimeFrameWeeks": 1,
      "AllowNegativeBudgetsToBeCarriedForward": "string",
      "AlternateProject": "string",
      "BankDocumentType": "string",
      "BudgetControlInterval": "string",
      "BudgetOverrunDefault": "string",
      "Calendar": "string",
      "CanCarryForwardRemainingBudgets": "string",
      "CanUseAlternateProjectBudget": "string",
      "CanUseBudgetControl": "string",
      "CanVerifyCostAgainstRemainingForecast": "string",
      "Category": "string",
      "CertifiedPayroll": "string",
      "ConstraintDate": "string",
      "ConstraintType": "string",
      "CustomerAccount": "string",
      "CustomerRetentionTermId": "string",
      "dataAreaId": "string",
      "Date": "string",
      "DateOfCreation": "string",
      "DefaultInvoiceAccount": "string",
      "DefaultOnSubprojects": "string",
      "DeliveryName": "Ava Chen",
      "Description": "string",
      "DimensionDisplayValue": "string",
      "DurationDeterminesEndDate": "string",
      "DurationInDays": 1,
      "Email": "ava@example.com",
      "EndDate1": "string",
      "EndTime": 1,
      "EstimateProjectID": "string",
      "ExtensionDate": "string",
      "ExternalRevision": "string",
      "Fax": "string",
      "FixedAssetNumber": "string",
      "Header": "string",
      "HourValidation": "string",
      "InvoiceCost": "string",
      "InvoicingMethod": "string",
      "IsActivityRequiredForExpenseForecast": "string",
      "IsActivityRequiredForExpenseTransaction": "string",
      "IsActivityRequiredForHourForecast": "string",
      "IsActivityRequiredForHourTransaction": "string",
      "IsActivityRequiredForItemForecast": "string",
      "IsActivityRequiredForItemTransaction": "string",
      "IsReadyForInvoicing": "string",
      "ItemValidation": "string",
      "JobIdentification": "string",
      "JobPayType": "string",
      "LedgerPostingSortPriority": "string",
      "LocationID": "string",
      "Milestone": "string",
      "MinimumTimeIncrement": 1,
      "Notes": "string",
      "ParentProject": "string",
      "PercentToRetain": 1,
      "PostingLevel": "string",
      "ProjectBudgetManagement": "string",
      "ProjectContractID": "string",
      "ProjectedEndDate": "string",
      "ProjectedStartDate": "string",
      "ProjectGroup": "string",
      "ProjectID": "string",
      "ProjectName": "Ava Chen",
      "ProjectOrTask": "string",
      "ProjectStage": "string",
      "ProjectTemplate": "string",
      "ProjectType": "string",
      "PSASchedIgnoreCalendar": "string",
      "RequisitionOrPurchaseOrderControl": "string",
      "SalesPriceGroup": "string",
      "SalesTaxGroup": "string",
      "ScheduleStatus": "string",
      "SearchPriority": "string",
      "SortingId1": "string",
      "SortingId2": "string",
      "SortingId3": "string",
      "StartDate1": "string",
      "StartTime": 1,
      "Status": "string",
      "SubprojectIDFormat": "string",
      "TaskCompletelyScheduled": "string",
      "Telephone": "string",
      "TemplateApplied": "string",
      "TimeMeasure": "string",
      "TotalEffortInHours": 1,
      "TrackCost": "string",
      "TransactionTypesControlled": "string",
      "Unit": "string",
      "WorkerArchitectPersonnelNumber": "string",
      "WorkerRespFinancialPersonnelNumber": "string",
      "WorkerResponsiblePersonnelNumber": "string",
      "WorkerRespSalesPersonnelNumber": "string",
      "ZakatContractAmendment": 1,
      "ZakatContractDate": "string",
      "ZakatContractPeriod": "string",
      "ZakatProjectValue": 1,
      "ZakatSubject": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Accounts action reference](actions/get-accounts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/microsoftDynamics365/latest/actions/get-accounts).

## Create Account



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftDynamics365/latest/actions/create-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftDynamics365/latest/actions/create-account', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "@odata": {
        "context": "string",
        "etag": "string"
      },
      "ActiveRevision": "string",
      "ActualEndDate": "string",
      "ActualStartDate": "string",
      "AlertTimeFrameWeeks": 1,
      "AllowNegativeBudgetsToBeCarriedForward": "string",
      "AlternateProject": "string",
      "BankDocumentType": "string",
      "BudgetControlInterval": "string",
      "BudgetOverrunDefault": "string",
      "Calendar": "string",
      "CanCarryForwardRemainingBudgets": "string",
      "CanUseAlternateProjectBudget": "string",
      "CanUseBudgetControl": "string",
      "CanVerifyCostAgainstRemainingForecast": "string",
      "Category": "string",
      "CertifiedPayroll": "string",
      "ConstraintDate": "string",
      "ConstraintType": "string",
      "CustomerAccount": "string",
      "CustomerRetentionTermId": "string",
      "dataAreaId": "string",
      "Date": "string",
      "DateOfCreation": "string",
      "DefaultInvoiceAccount": "string",
      "DefaultOnSubprojects": "string",
      "DeliveryName": "Ava Chen",
      "Description": "string",
      "DimensionDisplayValue": "string",
      "DurationDeterminesEndDate": "string",
      "DurationInDays": 1,
      "Email": "ava@example.com",
      "EndDate1": "string",
      "EndTime": 1,
      "EstimateProjectID": "string",
      "ExtensionDate": "string",
      "ExternalRevision": "string",
      "Fax": "string",
      "FixedAssetNumber": "string",
      "Header": "string",
      "HourValidation": "string",
      "InvoiceCost": "string",
      "InvoicingMethod": "string",
      "IsActivityRequiredForExpenseForecast": "string",
      "IsActivityRequiredForExpenseTransaction": "string",
      "IsActivityRequiredForHourForecast": "string",
      "IsActivityRequiredForHourTransaction": "string",
      "IsActivityRequiredForItemForecast": "string",
      "IsActivityRequiredForItemTransaction": "string",
      "IsReadyForInvoicing": "string",
      "ItemValidation": "string",
      "JobIdentification": "string",
      "JobPayType": "string",
      "LedgerPostingSortPriority": "string",
      "LocationID": "string",
      "Milestone": "string",
      "MinimumTimeIncrement": 1,
      "Notes": "string",
      "ParentProject": "string",
      "PercentToRetain": 1,
      "PostingLevel": "string",
      "ProjectBudgetManagement": "string",
      "ProjectContractID": "string",
      "ProjectedEndDate": "string",
      "ProjectedStartDate": "string",
      "ProjectGroup": "string",
      "ProjectID": "string",
      "ProjectName": "Ava Chen",
      "ProjectOrTask": "string",
      "ProjectStage": "string",
      "ProjectTemplate": "string",
      "ProjectType": "string",
      "PSASchedIgnoreCalendar": "string",
      "RequisitionOrPurchaseOrderControl": "string",
      "SalesPriceGroup": "string",
      "SalesTaxGroup": "string",
      "ScheduleStatus": "string",
      "SearchPriority": "string",
      "SortingId1": "string",
      "SortingId2": "string",
      "SortingId3": "string",
      "StartDate1": "string",
      "StartTime": 1,
      "Status": "string",
      "SubprojectIDFormat": "string",
      "TaskCompletelyScheduled": "string",
      "Telephone": "string",
      "TemplateApplied": "string",
      "TimeMeasure": "string",
      "TotalEffortInHours": 1,
      "TrackCost": "string",
      "TransactionTypesControlled": "string",
      "Unit": "string",
      "WorkerArchitectPersonnelNumber": "string",
      "WorkerRespFinancialPersonnelNumber": "string",
      "WorkerResponsiblePersonnelNumber": "string",
      "WorkerRespSalesPersonnelNumber": "string",
      "ZakatContractAmendment": 1,
      "ZakatContractDate": "string",
      "ZakatContractPeriod": "string",
      "ZakatProjectValue": 1,
      "ZakatSubject": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Account action reference](actions/create-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/microsoftDynamics365/latest/actions/create-account).
