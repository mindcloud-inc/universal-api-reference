# Microsoft Dynamics 365: Create Project



```
POST https://connect.mindcloud.co/v1/universal/microsoftDynamics365/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Dynamics 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftDynamics365/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dataAreaId": "string",
  "projectID": "string",
  "actualStartDate": "2026-05-07T12:00:00.000Z",
  "durationInDays": 1,
  "zakatContractAmendment": "0",
  "alertTimeFrameWeeks": "0",
  "projectStage": "Created"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftDynamics365/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dataAreaId": "string",
    "projectID": "string",
    "actualStartDate": "2026-05-07T12:00:00.000Z",
    "durationInDays": 1,
    "zakatContractAmendment": "0",
    "alertTimeFrameWeeks": "0",
    "projectStage": "Created"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dataAreaId` | string | yes |  |
| `projectID` | string | yes |  |
| `actualStartDate` | date | yes |  |
| `projectedStartDate` | date | no |  |
| `projectName` | string | no |  |
| `projectType` | string | no |  |
| `durationInDays` | number | yes |  |
| `workerResponsiblePersonnelNumber` | string | no | Project Manager |
| `workerRespSalesPersonnelNumber` | string | no | Sales |
| `workerRespFinancialPersonnelNumber` | string | no |  |
| `customerAccount` | string | no |  |
| `salesTaxGroup` | string | no |  |
| `projectGroup` | string | no |  |
| `status` | string | no | Default: `Active`. |
| `email` | string | no |  |
| `deliveryName` | string | no |  |
| `dateOfCreation` | date | no |  |
| `projectContractID` | string | no |  |
| `projectBudgetManagement` | string | no | Default: `Independent`. |
| `allowNegativeBudgetsToBeCarriedForward` | string | no |  |
| `certifiedPayroll` | string | no | Default: `No`. |
| `canVerifyCostAgainstRemainingForecast` | string | no | Yes / No Default: `No`. |
| `trackCost` | string | no | Default: `Actual`. |
| `bankDocumentType` | string | no |  |
| `dimensionDisplayValue` | string | no |  |
| `isActivityRequiredForHourForecast` | string | no |  |
| `sortingId1` | string | no |  |
| `sortingId2` | string | no |  |
| `calendar` | string | no | Default: `Default`. |
| `zakatContractAmendment` | number | yes | Default: `0`. |
| `locationID` | string | no |  |
| `isActivityRequiredForItemTransaction` | string | no |  |
| `zakatContractPeriod` | string | no |  |
| `parentProject` | string | no |  |
| `requisitionOrPurchaseOrderControl` | string | no | Default: `None`. |
| `constraintType` | string | no | Default: `AsSoonAsPossible`. |
| `alertTimeFrameWeeks` | number | yes | Default: `0`. |
| `projectStage` | string | yes | Default: `Created`. |
| `invoicingMethod` | string | no | Default: `Progress`. |
| `zakatProjectValue` | string | no |  |
| `constraintDate` | date | no |  |
| `budgetControlInterval` | string | no | Default: `TotalBudget`. |
| `percentToRetain` | number | no | Default: `0`. |
| `totalEffortInHours` | number | no | Default: `0`. |
| `zakatContractDate` | date | no |  |
| `isActivityRequiredForExpenseForecast` | string | no |  |
| `postingLevel` | string | no | Default: `Detail`. |
| `invoiceCost` | string | no | Default: `No`. |
| `timeMeasure` | string | no | Default: `Hour`. |
| `budgetOverrunDefault` | string | no | Default: `AllowOverruns`. |
| `extensionDate` | date | no |  |
| `startDate1` | date | no |  |
| `notes` | string | no |  |
| `description` | string | no |  |
| `minimumTimeIncrement` | number | no | Default: `0`. |
| `subprojectIDFormat` | string | no | Default: `-##`. |
| `searchPriority` | string | no |  |
| `canUseBudgetControl` | string | no | Default: `Yes`. |
| `itemValidation` | string | no |  |
| `taskCompletelyScheduled` | string | no | Default: `No`. |
| `durationDeterminesEndDate` | string | no | Default: `No`. |
| `isActivityRequiredForExpenseTransaction` | string | no | Default: `No`. |
| `unit` | string | no |  |
| `isActivityRequiredForItemForecast` | string | no | Default: `No`. |
| `hourValidation` | string | no | Default: `Amount`. |
| `salesPriceGroup` | string | no |  |
| `projectedEndDate` | string | no |  |
| `defaultOnSubprojects` | string | no | Default: `No`. |
| `actualEndDate` | string | no |  |
| `fixedAssetNumber` | string | no |  |
| `canUseAlternateProjectBudget` | string | no | Default: `No`. |
| `jobPayType` | string | no |  |
| `isReadyForInvoicing` | string | no | Default: `No`. |
| `workerArchitectPersonnelNumber` | string | no |  |
| `ledgerPostingSortPriority` | string | no | Default: `Categories`. |
| `telephone` | string | no |  |
| `customerRetentionTermId` | string | no |  |
| `pSASchedIgnoreCalendar` | string | no |  |
| `projectTemplate` | string | no |  |
| `defaultInvoiceAccount` | string | no |  |
| `jobIdentification` | string | no |  |
| `alternateProject` | string | no |  |
| `projectOrTask` | string | no |  |
| `header` | string | no |  |
| `isActivityRequiredForHourTransaction` | string | no |  |
| `scheduleStatus` | string | no |  |
| `milestone` | string | no |  |
| `externalRevision` | string | no | Default: `ORIG`. |
| `category` | string | no |  |
| `estimateProjectID` | string | no |  |
| `templateApplied` | string | no | Default: `No`. |
| `fax` | string | no |  |
| `sortingId3` | string | no |  |
| `activeRevision` | string | no |  |
| `zakatSubject` | string | no |  |
| `transactionTypesControlled` | string | no | Default: `RevenuesAndCosts`. |
| `canCarryForwardRemainingBudgets` | string | no | Default: `No`. |
| `date` | date | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Dynamics 365 API returns.

## Native endpoint

Through the native Microsoft Dynamics 365 API, this operation is `POST Projects` (base URL `{{credentials.baseURL}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

