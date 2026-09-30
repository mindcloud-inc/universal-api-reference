# Microsoft Dynamics 365: Patch Accounts



```
POST https://connect.mindcloud.co/v1/universal/microsoftDynamics365/latest/actions/patch-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Dynamics 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftDynamics365/latest/actions/patch-accounts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftDynamics365/latest/actions/patch-accounts', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customFields[]` | array | no |  |
| `customFields[].customKey` | string | no |  |
| `accountsId` | string | no |  |
| `customFields[].customValue` | string | no |  |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `@odata.context` | string |  |
| `@odata.etag` | string |  |
| `ActiveRevision` | string |  |
| `ActualEndDate` | string |  |
| `ActualStartDate` | string |  |
| `AlertTimeFrameWeeks` | number |  |
| `AllowNegativeBudgetsToBeCarriedForward` | string |  |
| `AlternateProject` | string |  |
| `BankDocumentType` | string |  |
| `BudgetControlInterval` | string |  |
| `BudgetOverrunDefault` | string |  |
| `Calendar` | string |  |
| `CanCarryForwardRemainingBudgets` | string |  |
| `CanUseAlternateProjectBudget` | string |  |
| `CanUseBudgetControl` | string |  |
| `CanVerifyCostAgainstRemainingForecast` | string |  |
| `Category` | string |  |
| `CertifiedPayroll` | string |  |
| `ConstraintDate` | string |  |
| `ConstraintType` | string |  |
| `CustomerAccount` | string |  |
| `CustomerRetentionTermId` | string |  |
| `dataAreaId` | string |  |
| `Date` | string |  |
| `DateOfCreation` | string |  |
| `DefaultInvoiceAccount` | string |  |
| `DefaultOnSubprojects` | string |  |
| `DeliveryName` | string |  |
| `Description` | string |  |
| `DimensionDisplayValue` | string |  |
| `DurationDeterminesEndDate` | string |  |
| `DurationInDays` | number |  |
| `Email` | string |  |
| `EndDate1` | string |  |
| `EndTime` | number |  |
| `EstimateProjectID` | string |  |
| `ExtensionDate` | string |  |
| `ExternalRevision` | string |  |
| `Fax` | string |  |
| `FixedAssetNumber` | string |  |
| `Header` | string |  |
| `HourValidation` | string |  |
| `InvoiceCost` | string |  |
| `InvoicingMethod` | string |  |
| `IsActivityRequiredForExpenseForecast` | string |  |
| `IsActivityRequiredForExpenseTransaction` | string |  |
| `IsActivityRequiredForHourForecast` | string |  |
| `IsActivityRequiredForHourTransaction` | string |  |
| `IsActivityRequiredForItemForecast` | string |  |
| `IsActivityRequiredForItemTransaction` | string |  |
| `IsReadyForInvoicing` | string |  |
| `ItemValidation` | string |  |
| `JobIdentification` | string |  |
| `JobPayType` | string |  |
| `LedgerPostingSortPriority` | string |  |
| `LocationID` | string |  |
| `Milestone` | string |  |
| `MinimumTimeIncrement` | number |  |
| `Notes` | string |  |
| `ParentProject` | string |  |
| `PercentToRetain` | number |  |
| `PostingLevel` | string |  |
| `ProjectBudgetManagement` | string |  |
| `ProjectContractID` | string |  |
| `ProjectedEndDate` | string |  |
| `ProjectedStartDate` | string |  |
| `ProjectGroup` | string |  |
| `ProjectID` | string |  |
| `ProjectName` | string |  |
| `ProjectOrTask` | string |  |
| `ProjectStage` | string |  |
| `ProjectTemplate` | string |  |
| `ProjectType` | string |  |
| `PSASchedIgnoreCalendar` | string |  |
| `RequisitionOrPurchaseOrderControl` | string |  |
| `SalesPriceGroup` | string |  |
| `SalesTaxGroup` | string |  |
| `ScheduleStatus` | string |  |
| `SearchPriority` | string |  |
| `SortingId1` | string |  |
| `SortingId2` | string |  |
| `SortingId3` | string |  |
| `StartDate1` | string |  |
| `StartTime` | number |  |
| `Status` | string |  |
| `SubprojectIDFormat` | string |  |
| `TaskCompletelyScheduled` | string |  |
| `Telephone` | string |  |
| `TemplateApplied` | string |  |
| `TimeMeasure` | string |  |
| `TotalEffortInHours` | number |  |
| `TrackCost` | string |  |
| `TransactionTypesControlled` | string |  |
| `Unit` | string |  |
| `WorkerArchitectPersonnelNumber` | string |  |
| `WorkerRespFinancialPersonnelNumber` | string |  |
| `WorkerResponsiblePersonnelNumber` | string |  |
| `WorkerRespSalesPersonnelNumber` | string |  |
| `ZakatContractAmendment` | number |  |
| `ZakatContractDate` | string |  |
| `ZakatContractPeriod` | string |  |
| `ZakatProjectValue` | number |  |
| `ZakatSubject` | string |  |

## Native endpoint

Through the native Microsoft Dynamics 365 API, this operation is `PATCH /accounts(:accountsId)` (base URL `{{credentials.baseURL}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/patch-accounts.md) for the provider-specific parameters and requirements.

