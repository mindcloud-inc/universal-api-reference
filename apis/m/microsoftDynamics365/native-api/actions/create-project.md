# Create Project with Microsoft Dynamics 365

## Endpoint

- **Method:** `POST`
- **Path:** `Projects`
- **Base URL:** `{baseURL}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataAreaId` | body | `string` | yes | — |
| `projectID` | body | `string` | yes | — |
| `actualStartDate` | body | `date` | yes | — |
| `projectedStartDate` | body | `date` | no | — |
| `projectName` | body | `string` | no | — |
| `projectType` | body | `string` | no | — |
| `durationInDays` | body | `number` | yes | — |
| `workerResponsiblePersonnelNumber` | body | `string` | no | Project Manager |
| `workerRespSalesPersonnelNumber` | body | `string` | no | Sales |
| `workerRespFinancialPersonnelNumber` | body | `string` | no | — |
| `customerAccount` | body | `string` | no | — |
| `salesTaxGroup` | body | `string` | no | — |
| `projectGroup` | body | `string` | no | — |
| `status` | body | `string` | no | — |
| `email` | body | `string` | no | — |
| `deliveryName` | body | `string` | no | — |
| `dateOfCreation` | body | `date` | no | — |
| `projectContractID` | body | `string` | no | — |
| `projectBudgetManagement` | body | `string` | no | — |
| `allowNegativeBudgetsToBeCarriedForward` | body | `string` | no | — |
| `certifiedPayroll` | body | `string` | no | — |
| `canVerifyCostAgainstRemainingForecast` | body | `string` | no | Yes / No |
| `trackCost` | body | `string` | no | — |
| `bankDocumentType` | body | `string` | no | — |
| `dimensionDisplayValue` | body | `string` | no | — |
| `isActivityRequiredForHourForecast` | body | `string` | no | — |
| `sortingId1` | body | `string` | no | — |
| `sortingId2` | body | `string` | no | — |
| `calendar` | body | `string` | no | — |
| `zakatContractAmendment` | body | `number` | yes | — |
| `locationID` | body | `string` | no | — |
| `isActivityRequiredForItemTransaction` | body | `string` | no | — |
| `zakatContractPeriod` | body | `string` | no | — |
| `parentProject` | body | `string` | no | — |
| `requisitionOrPurchaseOrderControl` | body | `string` | no | — |
| `constraintType` | body | `string` | no | — |
| `alertTimeFrameWeeks` | body | `number` | yes | — |
| `projectStage` | body | `string` | yes | — |
| `invoicingMethod` | body | `string` | no | — |
| `zakatProjectValue` | body | `string` | no | — |
| `constraintDate` | body | `date` | no | — |
| `budgetControlInterval` | body | `string` | no | — |
| `percentToRetain` | body | `number` | no | — |
| `totalEffortInHours` | body | `number` | no | — |
| `zakatContractDate` | body | `date` | no | — |
| `isActivityRequiredForExpenseForecast` | body | `string` | no | — |
| `postingLevel` | body | `string` | no | — |
| `invoiceCost` | body | `string` | no | — |
| `timeMeasure` | body | `string` | no | — |
| `budgetOverrunDefault` | body | `string` | no | — |
| `extensionDate` | body | `date` | no | — |
| `startDate1` | body | `date` | no | — |
| `notes` | body | `string` | no | — |
| `description` | body | `string` | no | — |
| `minimumTimeIncrement` | body | `number` | no | — |
| `subprojectIDFormat` | body | `string` | no | — |
| `searchPriority` | body | `string` | no | — |
| `canUseBudgetControl` | body | `string` | no | — |
| `itemValidation` | body | `string` | no | — |
| `taskCompletelyScheduled` | body | `string` | no | — |
| `durationDeterminesEndDate` | body | `string` | no | — |
| `isActivityRequiredForExpenseTransaction` | body | `string` | no | — |
| `unit` | body | `string` | no | — |
| `isActivityRequiredForItemForecast` | body | `string` | no | — |
| `hourValidation` | body | `string` | no | — |
| `salesPriceGroup` | body | `string` | no | — |
| `projectedEndDate` | body | `string` | no | — |
| `defaultOnSubprojects` | body | `string` | no | — |
| `actualEndDate` | body | `string` | no | — |
| `fixedAssetNumber` | body | `string` | no | — |
| `canUseAlternateProjectBudget` | body | `string` | no | — |
| `jobPayType` | body | `string` | no | — |
| `isReadyForInvoicing` | body | `string` | no | — |
| `workerArchitectPersonnelNumber` | body | `string` | no | — |
| `ledgerPostingSortPriority` | body | `string` | no | — |
| `telephone` | body | `string` | no | — |
| `customerRetentionTermId` | body | `string` | no | — |
| `pSASchedIgnoreCalendar` | body | `string` | no | — |
| `projectTemplate` | body | `string` | no | — |
| `defaultInvoiceAccount` | body | `string` | no | — |
| `jobIdentification` | body | `string` | no | — |
| `alternateProject` | body | `string` | no | — |
| `projectOrTask` | body | `string` | no | — |
| `header` | body | `string` | no | — |
| `isActivityRequiredForHourTransaction` | body | `string` | no | — |
| `scheduleStatus` | body | `string` | no | — |
| `milestone` | body | `string` | no | — |
| `externalRevision` | body | `string` | no | — |
| `category` | body | `string` | no | — |
| `estimateProjectID` | body | `string` | no | — |
| `templateApplied` | body | `string` | no | — |
| `fax` | body | `string` | no | — |
| `sortingId3` | body | `string` | no | — |
| `activeRevision` | body | `string` | no | — |
| `zakatSubject` | body | `string` | no | — |
| `transactionTypesControlled` | body | `string` | no | — |
| `canCarryForwardRemainingBudgets` | body | `string` | no | — |
| `date` | body | `date` | no | — |
