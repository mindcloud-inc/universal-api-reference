# Jotform: Login User

Creates a user session in Jotform.

```
POST https://connect.mindcloud.co/v1/universal/jotform/latest/actions/login-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jotform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jotform/latest/actions/login-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "password": "string",
  "username": "jane.doe"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jotform/latest/actions/login-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "password": "string",
    "username": "jane.doe"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `access` | string | no | Access level for the generated API key (readOnly/full). Default: `readOnly`. |
| `appName` | string | no | App label for the generated API key. Default: `MindCloud`. |
| `password` | string | yes | Jotform account password. |
| `username` | string | yes | Jotform account username. Example: `jane.doe`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "loginType": "string",
      "user": {
        "abandonedUser": {},
        "abJotformAITest": "string",
        "abPdfEditorOnepage": {},
        "abPdfPageLayout": {},
        "abTestKey": {},
        "accountInfoPercentage": {},
        "accountType": {
          "limits": {
            "aiAgents": 1,
            "aiAgentSms": 1,
            "aiChatbotAgents": 1,
            "aiChatbotConversations": 1,
            "aiConversations": 1,
            "aiKnowledgeBase": 1,
            "aiMessages": 1,
            "aiPhoneCall": 1,
            "aiSessions": 1,
            "fieldPerForm": 1,
            "formCount": 1,
            "overSubmissions": 1,
            "payments": 1,
            "signedDocuments": 1,
            "sslSubmissions": 1,
            "submissions": 1,
            "subusers": 1,
            "tickets": 1,
            "totalSubmissions": 1,
            "uploads": 1,
            "views": 1,
            "workflowRuns": 1
          },
          "name": "Ava Chen",
          "prettyName": "Ava Chen"
        },
        "accountUsage": {},
        "adyenEnable": {},
        "adyenReference": {},
        "aIAgentBetaAccepted": {},
        "aiAgentBetaUser": {},
        "aiAgentExistingUserAB": {},
        "aiAgentNewUserAB": {},
        "aiAppBuilderBetaUserAgreement": {},
        "aIAssistantModalSeen": {},
        "aiFormBuilderBetaUser": {},
        "aiFormBuilderBetaUserAgreement": {},
        "allowAutoresponders": {},
        "appBetaUser": {},
        "appPickerSideMode": {},
        "appPickerTooltipSeen": {},
        "audience": {},
        "autoDeleteApplyAll": {},
        "autoDeleteInterval": {},
        "autoDeleteStartDate": {},
        "autopilotBetaTestUser": "string",
        "avatarUrl": "https://example.com",
        "baaSubmissionID": {},
        "backToPaidCampaign": {},
        "backToPaidEmail": {},
        "backupEmail": {},
        "billing3dsData": {},
        "billingAccountBalance": {},
        "billingInformation": {},
        "billingPaymentMethod": {},
        "boardsBetaUser": {},
        "branding21": {},
        "builderPaymentListTestGroup": {},
        "cardForms": {},
        "ccpa": {},
        "checkHIPAAPassword": {},
        "checkoutPeriodOptionsVisibilityTest": {},
        "company": "string",
        "companyLogo": {},
        "companyRole": {},
        "companySize": {},
        "conditionEngineBetaUser": {},
        "convertedFromFormUser": {},
        "createdAt": "string",
        "customizedExperienceModal": {},
        "defaultJournalAdded": {},
        "defaultTheme": "string",
        "defaultThemeGroup": {},
        "disableNewUsercampaignInCampaignPeriod": {},
        "dismissOverduePaymentNotification": {},
        "displayHipaaEnforcementWarning": {},
        "donationBoxBetaAccepted": {},
        "doNotClone": {},
        "doNotShowBranding21Lightbox": {},
        "dontShowOrgModal": {},
        "dontShowPreviewTips": {},
        "education": {},
        "educationCampaign": {},
        "educationDiscountTestGroup": {},
        "email": "ava@example.com",
        "emailMessageVerification": {},
        "emailsAvailable": {},
        "enablePasswordExpiration": {},
        "encryptForms": {},
        "encryptionV2BetaAccepted": {},
        "enforceSignupOnPublish": {},
        "eoyDesignVersionTwo": {},
        "euOnly": "string",
        "exportSubmissionConfigVersion": {},
        "fastspringAccount": {},
        "favoriteWidgets": {},
        "fcmUnsubscribed": {},
        "folderLayout": {},
        "forcePasswordUpdate": {},
        "forcePasswordUpdateByCron": {},
        "formCount": 1,
        "formCountLimit": 1,
        "gdpr": {},
        "ghostMode": {},
        "gj": {},
        "goals": {},
        "gravatarURL": "https://example.com",
        "healthAppUser": {},
        "hideBetaBadges": {},
        "hipaaComplianceAnswerOnUpgrade": {},
        "hipaaComplienceAccountBoxOffer": {},
        "hipaaDowngradeEmail": {},
        "hIPAADowngradeScriptLastCheckedOn": {},
        "hipaaGracePeriod": {},
        "id": "string",
        "industry": "string",
        "inputTableBetaUser": {},
        "intentionalPublish": {},
        "intentionalPublishExistingUserAB": {},
        "intentionalPublishExistingUserABupdated": {},
        "intentionalPublishNewUserAB": {},
        "intentionalPublishNewUserABupdated": {},
        "intentionalPublishNewUsers": {},
        "isformCountLimitActive": true,
        "isHIPAA": "string",
        "isNewValidation": {},
        "isStrongPassword": true,
        "isVerified": "string",
        "jfAcademyBetaUser": {},
        "jobTitle": "string",
        "kvkk": {},
        "language": "string",
        "lastSeenAt": "string",
        "limitDialogNewDesign": {},
        "localeCurrencySymbol": {},
        "loginToGetSubmissions": "string",
        "loginToViewSubmissionRSS": "string",
        "loginToViewUploadedFiles": "string",
        "mfaPrimaryMethod": {},
        "mobileAssigneeIntroVersion": {},
        "mobileNextType": {},
        "mobilePublishShareButton": {},
        "mobileUserIntroVersion": {},
        "mobileUSInAppPurchase": {},
        "mobileUSInAppPurchaseSecond": {},
        "mobileUSInAppPurchaseThirdRound": {},
        "myformsModal": {},
        "name": "Ava Chen",
        "newGoogleSheetsUserGroup": {},
        "newInsertUpdateDataBetaUser": {},
        "newUserCampaignAssetsUK": {},
        "newUserCampaignAssetsUS": {},
        "newUsersCampaign": "string",
        "nonprofit": {},
        "notHipaaCompliantConsent": {},
        "organizationLogo": {},
        "overQuotaCampaign": {},
        "passwordChanged": true,
        "paymentCredentialCleanUp": {},
        "paymentReusableConnections": "string",
        "paypalBillingAgreement": {},
        "paypalBillingInformation": {},
        "paypalUniqueID": {},
        "pdfDesignerGroup": {},
        "pdfEditorTutorial": {},
        "pdfGeneratePdfGround": {},
        "phone": {},
        "phoneNumberVerified": {},
        "planType": {},
        "pricingTableCampaignColor": {},
        "promoteNDT": {},
        "pubintentBeta": {},
        "publicKey": {},
        "refApp": {},
        "referer": "string",
        "referrer": {},
        "region": "string",
        "regularFiftyDiscount": {},
        "remarketingInfo": {},
        "reSignBAAEnabled": {},
        "salesforceIntegrationUser": {},
        "securityAnswer": {},
        "securityQuestion": {},
        "senderEmails": {},
        "shortTermMonthlyToAnnualPlanCampaign": {},
        "showFormCountStats": true,
        "showJotFormBrandingOnReport": {},
        "showJotFormLogo": {},
        "showJotFormPowered": "string",
        "showNdtPromotionModal": {},
        "showTemplateSuggestionModal": {},
        "signTeams": {},
        "spreadsheets": {},
        "squareBlogBannerID": {},
        "squareWarningEnabled": {},
        "ssvAutoResponderEmailTest": {},
        "status": "string",
        "storeCountryCode": {},
        "stripeActive": {},
        "stripeId": {},
        "stripeLocationChecked": {},
        "stripeSource": {},
        "stripeSubscription": {},
        "subscriptionPaymentsAllowed": {},
        "subUserMode": {},
        "suspendReason": {},
        "switchLanguageOffer": {},
        "tablesIntroVideoShown": {},
        "taxData": {},
        "teamFeedbackSeen": {},
        "teamsBetaUser": {},
        "termsPdf": {},
        "textMessageVerification": {},
        "theme": {},
        "timeFormat": {},
        "timeZone": "string",
        "turkishSupport": {},
        "unreadSupportAnswerCount": {},
        "updatedAt": "string",
        "userActivity": {},
        "userData": {},
        "username": "Ava Chen",
        "usersCampaignExtended": {},
        "verifyToChangeEmail": {},
        "walkthroughOffered": {},
        "webhooks": {},
        "website": "string",
        "workflowVariation": {},
        "zapierConnectedOn": {},
        "zapierToken": {}
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `loginType` | string |  |
| `user.abandonedUser` | object |  |
| `user.abJotformAITest` | string |  |
| `user.abPdfEditorOnepage` | object |  |
| `user.abPdfPageLayout` | object |  |
| `user.abTestKey` | object |  |
| `user.accountInfoPercentage` | object |  |
| `user.accountType.limits.aiAgents` | number |  |
| `user.accountType.limits.aiAgentSms` | number |  |
| `user.accountType.limits.aiChatbotAgents` | number |  |
| `user.accountType.limits.aiChatbotConversations` | number |  |
| `user.accountType.limits.aiConversations` | number |  |
| `user.accountType.limits.aiKnowledgeBase` | number |  |
| `user.accountType.limits.aiMessages` | number |  |
| `user.accountType.limits.aiPhoneCall` | number |  |
| `user.accountType.limits.aiSessions` | number |  |
| `user.accountType.limits.fieldPerForm` | number |  |
| `user.accountType.limits.formCount` | number |  |
| `user.accountType.limits.overSubmissions` | number |  |
| `user.accountType.limits.payments` | number |  |
| `user.accountType.limits.signedDocuments` | number |  |
| `user.accountType.limits.sslSubmissions` | number |  |
| `user.accountType.limits.submissions` | number |  |
| `user.accountType.limits.subusers` | number |  |
| `user.accountType.limits.tickets` | number |  |
| `user.accountType.limits.totalSubmissions` | number |  |
| `user.accountType.limits.uploads` | number |  |
| `user.accountType.limits.views` | number |  |
| `user.accountType.limits.workflowRuns` | number |  |
| `user.accountType.name` | string |  |
| `user.accountType.prettyName` | string |  |
| `user.accountUsage` | object |  |
| `user.adyenEnable` | object |  |
| `user.adyenReference` | object |  |
| `user.aIAgentBetaAccepted` | object |  |
| `user.aiAgentBetaUser` | object |  |
| `user.aiAgentExistingUserAB` | object |  |
| `user.aiAgentNewUserAB` | object |  |
| `user.aiAppBuilderBetaUserAgreement` | object |  |
| `user.aIAssistantModalSeen` | object |  |
| `user.aiFormBuilderBetaUser` | object |  |
| `user.aiFormBuilderBetaUserAgreement` | object |  |
| `user.allowAutoresponders` | object |  |
| `user.appBetaUser` | object |  |
| `user.appPickerSideMode` | object |  |
| `user.appPickerTooltipSeen` | object |  |
| `user.audience` | object |  |
| `user.autoDeleteApplyAll` | object |  |
| `user.autoDeleteInterval` | object |  |
| `user.autoDeleteStartDate` | object |  |
| `user.autopilotBetaTestUser` | string |  |
| `user.avatarUrl` | string |  |
| `user.baaSubmissionID` | object |  |
| `user.backToPaidCampaign` | object |  |
| `user.backToPaidEmail` | object |  |
| `user.backupEmail` | object |  |
| `user.billing3dsData` | object |  |
| `user.billingAccountBalance` | object |  |
| `user.billingInformation` | object |  |
| `user.billingPaymentMethod` | object |  |
| `user.boardsBetaUser` | object |  |
| `user.branding21` | object |  |
| `user.builderPaymentListTestGroup` | object |  |
| `user.cardForms` | object |  |
| `user.ccpa` | object |  |
| `user.checkHIPAAPassword` | object |  |
| `user.checkoutPeriodOptionsVisibilityTest` | object |  |
| `user.company` | string |  |
| `user.companyLogo` | object |  |
| `user.companyRole` | object |  |
| `user.companySize` | object |  |
| `user.conditionEngineBetaUser` | object |  |
| `user.convertedFromFormUser` | object |  |
| `user.createdAt` | string |  |
| `user.customizedExperienceModal` | object |  |
| `user.defaultJournalAdded` | object |  |
| `user.defaultTheme` | string |  |
| `user.defaultThemeGroup` | object |  |
| `user.disableNewUsercampaignInCampaignPeriod` | object |  |
| `user.dismissOverduePaymentNotification` | object |  |
| `user.displayHipaaEnforcementWarning` | object |  |
| `user.donationBoxBetaAccepted` | object |  |
| `user.doNotClone` | object |  |
| `user.doNotShowBranding21Lightbox` | object |  |
| `user.dontShowOrgModal` | object |  |
| `user.dontShowPreviewTips` | object |  |
| `user.education` | object |  |
| `user.educationCampaign` | object |  |
| `user.educationDiscountTestGroup` | object |  |
| `user.email` | string |  |
| `user.emailMessageVerification` | object |  |
| `user.emailsAvailable` | object |  |
| `user.enablePasswordExpiration` | object |  |
| `user.encryptForms` | object |  |
| `user.encryptionV2BetaAccepted` | object |  |
| `user.enforceSignupOnPublish` | object |  |
| `user.eoyDesignVersionTwo` | object |  |
| `user.euOnly` | string |  |
| `user.exportSubmissionConfigVersion` | object |  |
| `user.fastspringAccount` | object |  |
| `user.favoriteWidgets` | object |  |
| `user.fcmUnsubscribed` | object |  |
| `user.folderLayout` | object |  |
| `user.forcePasswordUpdate` | object |  |
| `user.forcePasswordUpdateByCron` | object |  |
| `user.formCount` | number |  |
| `user.formCountLimit` | number |  |
| `user.gdpr` | object |  |
| `user.ghostMode` | object |  |
| `user.gj` | object |  |
| `user.goals` | object |  |
| `user.gravatarURL` | string |  |
| `user.healthAppUser` | object |  |
| `user.hideBetaBadges` | object |  |
| `user.hipaaComplianceAnswerOnUpgrade` | object |  |
| `user.hipaaComplienceAccountBoxOffer` | object |  |
| `user.hipaaDowngradeEmail` | object |  |
| `user.hIPAADowngradeScriptLastCheckedOn` | object |  |
| `user.hipaaGracePeriod` | object |  |
| `user.id` | string |  |
| `user.industry` | string |  |
| `user.inputTableBetaUser` | object |  |
| `user.intentionalPublish` | object |  |
| `user.intentionalPublishExistingUserAB` | object |  |
| `user.intentionalPublishExistingUserABupdated` | object |  |
| `user.intentionalPublishNewUserAB` | object |  |
| `user.intentionalPublishNewUserABupdated` | object |  |
| `user.intentionalPublishNewUsers` | object |  |
| `user.isformCountLimitActive` | boolean |  |
| `user.isHIPAA` | string |  |
| `user.isNewValidation` | object |  |
| `user.isStrongPassword` | boolean |  |
| `user.isVerified` | string |  |
| `user.jfAcademyBetaUser` | object |  |
| `user.jobTitle` | string |  |
| `user.kvkk` | object |  |
| `user.language` | string |  |
| `user.lastSeenAt` | string |  |
| `user.limitDialogNewDesign` | object |  |
| `user.localeCurrencySymbol` | object |  |
| `user.loginToGetSubmissions` | string |  |
| `user.loginToViewSubmissionRSS` | string |  |
| `user.loginToViewUploadedFiles` | string |  |
| `user.mfaPrimaryMethod` | object |  |
| `user.mobileAssigneeIntroVersion` | object |  |
| `user.mobileNextType` | object |  |
| `user.mobilePublishShareButton` | object |  |
| `user.mobileUserIntroVersion` | object |  |
| `user.mobileUSInAppPurchase` | object |  |
| `user.mobileUSInAppPurchaseSecond` | object |  |
| `user.mobileUSInAppPurchaseThirdRound` | object |  |
| `user.myformsModal` | object |  |
| `user.name` | string |  |
| `user.newGoogleSheetsUserGroup` | object |  |
| `user.newInsertUpdateDataBetaUser` | object |  |
| `user.newUserCampaignAssetsUK` | object |  |
| `user.newUserCampaignAssetsUS` | object |  |
| `user.newUsersCampaign` | string |  |
| `user.nonprofit` | object |  |
| `user.notHipaaCompliantConsent` | object |  |
| `user.organizationLogo` | object |  |
| `user.overQuotaCampaign` | object |  |
| `user.passwordChanged` | boolean |  |
| `user.paymentCredentialCleanUp` | object |  |
| `user.paymentReusableConnections` | string |  |
| `user.paypalBillingAgreement` | object |  |
| `user.paypalBillingInformation` | object |  |
| `user.paypalUniqueID` | object |  |
| `user.pdfDesignerGroup` | object |  |
| `user.pdfEditorTutorial` | object |  |
| `user.pdfGeneratePdfGround` | object |  |
| `user.phone` | object |  |
| `user.phoneNumberVerified` | object |  |
| `user.planType` | object |  |
| `user.pricingTableCampaignColor` | object |  |
| `user.promoteNDT` | object |  |
| `user.pubintentBeta` | object |  |
| `user.publicKey` | object |  |
| `user.refApp` | object |  |
| `user.referer` | string |  |
| `user.referrer` | object |  |
| `user.region` | string |  |
| `user.regularFiftyDiscount` | object |  |
| `user.remarketingInfo` | object |  |
| `user.reSignBAAEnabled` | object |  |
| `user.salesforceIntegrationUser` | object |  |
| `user.securityAnswer` | object |  |
| `user.securityQuestion` | object |  |
| `user.senderEmails` | object |  |
| `user.shortTermMonthlyToAnnualPlanCampaign` | object |  |
| `user.showFormCountStats` | boolean |  |
| `user.showJotFormBrandingOnReport` | object |  |
| `user.showJotFormLogo` | object |  |
| `user.showJotFormPowered` | string |  |
| `user.showNdtPromotionModal` | object |  |
| `user.showTemplateSuggestionModal` | object |  |
| `user.signTeams` | object |  |
| `user.spreadsheets` | object |  |
| `user.squareBlogBannerID` | object |  |
| `user.squareWarningEnabled` | object |  |
| `user.ssvAutoResponderEmailTest` | object |  |
| `user.status` | string |  |
| `user.storeCountryCode` | object |  |
| `user.stripeActive` | object |  |
| `user.stripeId` | object |  |
| `user.stripeLocationChecked` | object |  |
| `user.stripeSource` | object |  |
| `user.stripeSubscription` | object |  |
| `user.subscriptionPaymentsAllowed` | object |  |
| `user.subUserMode` | object |  |
| `user.suspendReason` | object |  |
| `user.switchLanguageOffer` | object |  |
| `user.tablesIntroVideoShown` | object |  |
| `user.taxData` | object |  |
| `user.teamFeedbackSeen` | object |  |
| `user.teamsBetaUser` | object |  |
| `user.termsPdf` | object |  |
| `user.textMessageVerification` | object |  |
| `user.theme` | object |  |
| `user.timeFormat` | object |  |
| `user.timeZone` | string |  |
| `user.turkishSupport` | object |  |
| `user.unreadSupportAnswerCount` | object |  |
| `user.updatedAt` | string |  |
| `user.userActivity` | object |  |
| `user.userData` | object |  |
| `user.username` | string |  |
| `user.usersCampaignExtended` | object |  |
| `user.verifyToChangeEmail` | object |  |
| `user.walkthroughOffered` | object |  |
| `user.webhooks` | object |  |
| `user.website` | string |  |
| `user.workflowVariation` | object |  |
| `user.zapierConnectedOn` | object |  |
| `user.zapierToken` | object |  |

## Native endpoint

Through the native Jotform API, this operation is `POST /user/login` (base URL `https://api.jotform.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/login-user.md) for the provider-specific parameters and requirements.

