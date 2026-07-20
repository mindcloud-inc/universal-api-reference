# Productive.io: List Organizations

Retrieves organizations from your Productive.io account.

```
GET https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/list-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productive.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/list-organizations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/list-organizations?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "addons": [
          "string"
        ],
        "aiEnabled": true,
        "allowTimeOff": true,
        "allowUserEmail": true,
        "analyticsUid": "string",
        "autotrackingScheduleId": 1,
        "avatarUrl": "https://example.com",
        "billingEmail": "ava@example.com",
        "bookedDemo": true,
        "conflictResolverActive": true,
        "currency": "string",
        "currencyDefault": "string",
        "currencyFormatId": 1,
        "currencyNormalized": "string",
        "customerSuccessSpecialistId": "string",
        "dateFormatId": 1,
        "dealSettings": {
          "advancedMode": true,
          "budgetWarning": "string",
          "clientAccess": true,
          "createOpenHoursOpenExpenses": true,
          "designatedApprover": true,
          "expenseApproval": true,
          "roundingIntervalId": "string",
          "roundingMethodId": "string",
          "timeApproval": true,
          "trackingTypeId": 1,
          "validateExpenseWhenClosing": true
        },
        "decimalPlacesId": 1,
        "deliveredBudgetRecognitionDateId": 1,
        "domainVerified": true,
        "dueDays": 1,
        "emailDomainName": "ava@example.com",
        "emailKey": "ava@example.com",
        "emailLocalName": "ava@example.com",
        "emailSenderName": "ava@example.com",
        "emailTypeId": 1,
        "erectorId": 1,
        "exchangeRateProviderId": 1,
        "expenseMarkup": 1,
        "expenseSettings": {
          "markup": 1,
          "payment": true,
          "reimbursement": true
        },
        "facilityCosts": 1,
        "facilityCostsDefault": 1,
        "facilityCostsNormalized": 1,
        "financialMonthLockingDate": 1,
        "financialMonthLockingPartialEdit": true,
        "flags": {
          "aiAgentAiCreditsAuthorization": true,
          "aiReports": true,
          "allowBookingsOutsideBudgetDate": true,
          "applyDealScenario": true,
          "archiveServiceTypes": true,
          "automationsRunNow": true,
          "convertDateParamsToPersonTimezone": true,
          "dealForecastingChartUpdate": true,
          "dealFunnelReportPermission": true,
          "dealMultipleSalesPipelines": true,
          "dealProposals": true,
          "dealServicesRedesign": true,
          "dealWizardRemoveProjectStep": true,
          "enableAICreditsUsageLimitation": true,
          "enableBudgetViewSharing": true,
          "enableDealViewSharing": true,
          "hideResourcePlannerWithoutPermissions": true,
          "lucinTest": true,
          "membershipNotificationRefactor": true,
          "newDesktopTimer": true,
          "noIncludesOnPreferencesPatch": true,
          "peopleCustomFieldsMigration": true,
          "projectNavigationRedesign": true,
          "rateCardPermissions": true,
          "reactionsInDocsComments": true,
          "reducedDashboardShareTypes": true,
          "removeTags": true,
          "reportServiceFilterExtendedScope": true,
          "resolvedPermissions": true,
          "resourcingBookingContextMenu": true,
          "resourcingDisablePendingBookings": true,
          "roundingSettingsOnDeal": true,
          "skipDelayedBroadcast": true,
          "templatesTypesAndCreators": true,
          "timeEntryApprovePermissionsSync": true,
          "timerPolicyUpdate": true
        },
        "forceSingleSignOn": true,
        "forceTwoFactorAuth": true,
        "invitationToken": "string",
        "invoiceRoundingMethodId": 1,
        "invoiceTimesheetExportDisplayCreatedBy": true,
        "invoiceTimesheetExportDisplayDateCreated": true,
        "invoiceTimesheetExportDisplayDescription": true,
        "invoiceTimesheetExportDisplayOrganizationLogo": true,
        "invoiceTimesheetExportDisplayTimePeriod": true,
        "invoiceTimesheetExportDisplayTotalCount": true,
        "invoiceTimesheetExportFormat": "string",
        "invoiceTimesheetExportOrientation": "string",
        "invoiceTimesheetExportPageSize": "string",
        "invoiceTimesheetExportReportId": "string",
        "limitedServiceTypes": true,
        "locale": "string",
        "manDayMinutes": 1,
        "metrics": "string",
        "name": "Ava Chen",
        "numberFormatId": 1,
        "onboardingProgress": "string",
        "openBudgetRecognitionDateId": 1,
        "organizationTypeId": 1,
        "originalAvatarUrl": "https://example.com",
        "overhead": true,
        "overheadAmortizationPeriod": 1,
        "overheadRecalculationDay": 1,
        "overheadSubsidiarySwitchedAt": "string",
        "overheadTypeId": 1,
        "quickStartConfig": "string",
        "removeBranding": true,
        "requestForResourceEnabled": true,
        "revenueRecognitionTypeId": 1,
        "roundingIntervalId": "string",
        "roundingMethodId": 1,
        "sampleDataImportedAt": "string",
        "sampleDataRevertedAt": "string",
        "scimBearerToken": "string",
        "selfAttribution": "string",
        "selfAttributionComment": "string",
        "singleSignOn": true,
        "subsidiaryCount": 1,
        "timeDisplayId": 1,
        "timeFormatId": 1,
        "timeLocking": true,
        "timeLockingInterval": "string",
        "timeLockingPeriodId": "string",
        "timeLockingReminders": "string",
        "timeReminderAt": 1,
        "timeReminderCondition": 1,
        "timeReminderId": 1,
        "timeReminders": true,
        "timesheetSubmission": true,
        "timesheetSubmissionReminders": true,
        "timesheetSubmissionSettings": {
          "reminderAt": "string",
          "reminderId": "string"
        },
        "timeTrackingPoliciesEnabled": true,
        "timeZone": "string",
        "verificationStatusId": 1,
        "verifiedAt": "string",
        "weekStartDayId": 1,
        "weight": 1,
        "workingHours": [
          1
        ]
      },
      "id": "string",
      "relationships": {
        "company": {
          "meta": {
            "included": true
          }
        },
        "organizationSubscription": {
          "meta": {
            "included": true
          }
        },
        "owner": {
          "meta": {
            "included": true
          }
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.addons` | array<string> |  |
| `attributes.aiEnabled` | boolean |  |
| `attributes.allowTimeOff` | boolean |  |
| `attributes.allowUserEmail` | boolean |  |
| `attributes.analyticsUid` | string |  |
| `attributes.autotrackingScheduleId` | number |  |
| `attributes.avatarUrl` | string |  |
| `attributes.billingEmail` | string |  |
| `attributes.bookedDemo` | boolean |  |
| `attributes.conflictResolverActive` | boolean |  |
| `attributes.currency` | string |  |
| `attributes.currencyDefault` | string |  |
| `attributes.currencyFormatId` | number |  |
| `attributes.currencyNormalized` | string |  |
| `attributes.customerSuccessSpecialistId` | string |  |
| `attributes.dateFormatId` | number |  |
| `attributes.dealSettings.advancedMode` | boolean |  |
| `attributes.dealSettings.budgetWarning` | string |  |
| `attributes.dealSettings.clientAccess` | boolean |  |
| `attributes.dealSettings.createOpenHoursOpenExpenses` | boolean |  |
| `attributes.dealSettings.designatedApprover` | boolean |  |
| `attributes.dealSettings.expenseApproval` | boolean |  |
| `attributes.dealSettings.roundingIntervalId` | string |  |
| `attributes.dealSettings.roundingMethodId` | string |  |
| `attributes.dealSettings.timeApproval` | boolean |  |
| `attributes.dealSettings.trackingTypeId` | number |  |
| `attributes.dealSettings.validateExpenseWhenClosing` | boolean |  |
| `attributes.decimalPlacesId` | number |  |
| `attributes.deliveredBudgetRecognitionDateId` | number |  |
| `attributes.domainVerified` | boolean |  |
| `attributes.dueDays` | number |  |
| `attributes.emailDomainName` | string |  |
| `attributes.emailKey` | string |  |
| `attributes.emailLocalName` | string |  |
| `attributes.emailSenderName` | string |  |
| `attributes.emailTypeId` | number |  |
| `attributes.erectorId` | number |  |
| `attributes.exchangeRateProviderId` | number |  |
| `attributes.expenseMarkup` | number |  |
| `attributes.expenseSettings.markup` | number |  |
| `attributes.expenseSettings.payment` | boolean |  |
| `attributes.expenseSettings.reimbursement` | boolean |  |
| `attributes.facilityCosts` | number |  |
| `attributes.facilityCostsDefault` | number |  |
| `attributes.facilityCostsNormalized` | number |  |
| `attributes.financialMonthLockingDate` | number |  |
| `attributes.financialMonthLockingPartialEdit` | boolean |  |
| `attributes.flags.aiAgentAiCreditsAuthorization` | boolean |  |
| `attributes.flags.aiReports` | boolean |  |
| `attributes.flags.allowBookingsOutsideBudgetDate` | boolean |  |
| `attributes.flags.applyDealScenario` | boolean |  |
| `attributes.flags.archiveServiceTypes` | boolean |  |
| `attributes.flags.automationsRunNow` | boolean |  |
| `attributes.flags.convertDateParamsToPersonTimezone` | boolean |  |
| `attributes.flags.dealForecastingChartUpdate` | boolean |  |
| `attributes.flags.dealFunnelReportPermission` | boolean |  |
| `attributes.flags.dealMultipleSalesPipelines` | boolean |  |
| `attributes.flags.dealProposals` | boolean |  |
| `attributes.flags.dealServicesRedesign` | boolean |  |
| `attributes.flags.dealWizardRemoveProjectStep` | boolean |  |
| `attributes.flags.enableAICreditsUsageLimitation` | boolean |  |
| `attributes.flags.enableBudgetViewSharing` | boolean |  |
| `attributes.flags.enableDealViewSharing` | boolean |  |
| `attributes.flags.hideResourcePlannerWithoutPermissions` | boolean |  |
| `attributes.flags.lucinTest` | boolean |  |
| `attributes.flags.membershipNotificationRefactor` | boolean |  |
| `attributes.flags.newDesktopTimer` | boolean |  |
| `attributes.flags.noIncludesOnPreferencesPatch` | boolean |  |
| `attributes.flags.peopleCustomFieldsMigration` | boolean |  |
| `attributes.flags.projectNavigationRedesign` | boolean |  |
| `attributes.flags.rateCardPermissions` | boolean |  |
| `attributes.flags.reactionsInDocsComments` | boolean |  |
| `attributes.flags.reducedDashboardShareTypes` | boolean |  |
| `attributes.flags.removeTags` | boolean |  |
| `attributes.flags.reportServiceFilterExtendedScope` | boolean |  |
| `attributes.flags.resolvedPermissions` | boolean |  |
| `attributes.flags.resourcingBookingContextMenu` | boolean |  |
| `attributes.flags.resourcingDisablePendingBookings` | boolean |  |
| `attributes.flags.roundingSettingsOnDeal` | boolean |  |
| `attributes.flags.skipDelayedBroadcast` | boolean |  |
| `attributes.flags.templatesTypesAndCreators` | boolean |  |
| `attributes.flags.timeEntryApprovePermissionsSync` | boolean |  |
| `attributes.flags.timerPolicyUpdate` | boolean |  |
| `attributes.forceSingleSignOn` | boolean |  |
| `attributes.forceTwoFactorAuth` | boolean |  |
| `attributes.invitationToken` | string |  |
| `attributes.invoiceRoundingMethodId` | number |  |
| `attributes.invoiceTimesheetExportDisplayCreatedBy` | boolean |  |
| `attributes.invoiceTimesheetExportDisplayDateCreated` | boolean |  |
| `attributes.invoiceTimesheetExportDisplayDescription` | boolean |  |
| `attributes.invoiceTimesheetExportDisplayOrganizationLogo` | boolean |  |
| `attributes.invoiceTimesheetExportDisplayTimePeriod` | boolean |  |
| `attributes.invoiceTimesheetExportDisplayTotalCount` | boolean |  |
| `attributes.invoiceTimesheetExportFormat` | string |  |
| `attributes.invoiceTimesheetExportOrientation` | string |  |
| `attributes.invoiceTimesheetExportPageSize` | string |  |
| `attributes.invoiceTimesheetExportReportId` | string |  |
| `attributes.limitedServiceTypes` | boolean |  |
| `attributes.locale` | string |  |
| `attributes.manDayMinutes` | number |  |
| `attributes.metrics` | string |  |
| `attributes.name` | string |  |
| `attributes.numberFormatId` | number |  |
| `attributes.onboardingProgress` | string |  |
| `attributes.openBudgetRecognitionDateId` | number |  |
| `attributes.organizationTypeId` | number |  |
| `attributes.originalAvatarUrl` | string |  |
| `attributes.overhead` | boolean |  |
| `attributes.overheadAmortizationPeriod` | number |  |
| `attributes.overheadRecalculationDay` | number |  |
| `attributes.overheadSubsidiarySwitchedAt` | string |  |
| `attributes.overheadTypeId` | number |  |
| `attributes.quickStartConfig` | string |  |
| `attributes.removeBranding` | boolean |  |
| `attributes.requestForResourceEnabled` | boolean |  |
| `attributes.revenueRecognitionTypeId` | number |  |
| `attributes.roundingIntervalId` | string |  |
| `attributes.roundingMethodId` | number |  |
| `attributes.sampleDataImportedAt` | string |  |
| `attributes.sampleDataRevertedAt` | string |  |
| `attributes.scimBearerToken` | string |  |
| `attributes.selfAttribution` | string |  |
| `attributes.selfAttributionComment` | string |  |
| `attributes.singleSignOn` | boolean |  |
| `attributes.subsidiaryCount` | number |  |
| `attributes.timeDisplayId` | number |  |
| `attributes.timeFormatId` | number |  |
| `attributes.timeLocking` | boolean |  |
| `attributes.timeLockingInterval` | string |  |
| `attributes.timeLockingPeriodId` | string |  |
| `attributes.timeLockingReminders` | string |  |
| `attributes.timeReminderAt` | number |  |
| `attributes.timeReminderCondition` | number |  |
| `attributes.timeReminderId` | number |  |
| `attributes.timeReminders` | boolean |  |
| `attributes.timesheetSubmission` | boolean |  |
| `attributes.timesheetSubmissionReminders` | boolean |  |
| `attributes.timesheetSubmissionSettings.reminderAt` | string |  |
| `attributes.timesheetSubmissionSettings.reminderId` | string |  |
| `attributes.timeTrackingPoliciesEnabled` | boolean |  |
| `attributes.timeZone` | string |  |
| `attributes.verificationStatusId` | number |  |
| `attributes.verifiedAt` | string |  |
| `attributes.weekStartDayId` | number |  |
| `attributes.weight` | number |  |
| `attributes.workingHours` | array<number> |  |
| `id` | string |  |
| `relationships.company.meta.included` | boolean |  |
| `relationships.organizationSubscription.meta.included` | boolean |  |
| `relationships.owner.meta.included` | boolean |  |
| `type` | string |  |

## Native endpoint

Through the native Productive.io API, this operation is `GET /organizations` (base URL `https://api.productive.io/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-organizations.md) for the provider-specific parameters and requirements.

