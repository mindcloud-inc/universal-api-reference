# Raklet: Get organisation settings



```
GET https://connect.mindcloud.co/v1/universal/raklet/latest/actions/get-organisation-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raklet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/raklet/latest/actions/get-organisation-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/raklet/latest/actions/get-organisation-settings?${params}`, {
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
      "activeUntil": {},
      "applicationFormAgreement": {},
      "applicationFormBenefits": {},
      "applicationFormFooter": {},
      "applicationFormHeader": {},
      "applicationFormIsAddressEnabled": true,
      "applicationFormIsBirthDateEnabled": true,
      "applicationFormIsBirthPlaceEnabled": true,
      "applicationFormIsCommentsEnabled": true,
      "applicationFormIsGenderEnabled": true,
      "applicationFormIsNationalityEnabled": true,
      "applicationFormIsTaxNumberEnabled": true,
      "applicationFormIsUnder18ControlEnabled": true,
      "applicationFormRegistrationFee": 1,
      "applicationFormTitle": {},
      "balance": 1,
      "commissionFee": 1,
      "commissionFeeCurrency": 1,
      "commissionRate": 1,
      "createdOn": "string",
      "creditCardProcessor": 1,
      "currency": 1,
      "defaultAddressCountry": "string",
      "defaultEmailIdentityId": "ava@example.com",
      "defaultPhoneCountryCode": "string",
      "defaultSmsIdentityId": "string",
      "googleAnalyticsTrackerId": {},
      "id": "string",
      "invoiceAddress": {},
      "isApplicationFormEnabled": true,
      "isCityListVisible": true,
      "isCompanyListVisible": true,
      "isCountryListVisible": true,
      "isCustomPaymentEnabled": true,
      "isDeleted": true,
      "isDonationEnabled": true,
      "isJobPostingsEnabled": true,
      "isLoginPasswordEnabled": true,
      "isLoginSmsEnabled": true,
      "isLoginSocialNetworkEnabled": true,
      "isLoginTwoFactorEnabled": true,
      "isLoginWithOneTimeLoginEnabled": true,
      "isMemberListVisible": true,
      "isOfferedServicesEnabled": true,
      "isOnlineCreditCardEnabled": true,
      "isPaymentEnabled": true,
      "isSchoolListVisible": true,
      "isSectorListVisible": true,
      "isTermsOfUseRequiredForAccess": true,
      "isWeeklyNewsletterAnnouncements": true,
      "isWeeklyNewsletterDonationCampaigns": true,
      "isWeeklyNewsletterEnabled": true,
      "isWeeklyNewsletterJobOffers": true,
      "isWeeklyNewsletterJobSeekers": true,
      "isWeeklyNewsletterMemberDebt": true,
      "isWeeklyNewsletterMemberUnreadMessages": true,
      "isWeeklyNewsletterNewMembersEnabled": true,
      "isWeeklyNewsletterServices": true,
      "language": "string",
      "legalEntityOwnersVerificationDocumentUrl": {},
      "legalEntityVerificationDocumentUrl": {},
      "loginPageTitle": {},
      "logoHeight": 1,
      "logoUrl": "https://example.com",
      "logoWidth": 1,
      "memberNoType": 1,
      "membershipTerms": {},
      "name": "Ava Chen",
      "onlineCreditCardSubMerchantId": {},
      "organisationColor1": "string",
      "organisationColor2": {},
      "organisationSupportEmail": "ava@example.com",
      "organisationSupportPhone": "string",
      "paymentFooter": {},
      "paymentHeader": {},
      "permalink": "https://example.com",
      "shortName": "Ava Chen",
      "smsIsEnabled": true,
      "smsProfit": 1,
      "state": 1,
      "stripeCustomerId": "string",
      "stripePlanId": {},
      "termsOfUse2App": {},
      "termsOfUseApp": {},
      "timeZoneId": "string",
      "totalCost": 1,
      "totalProfit": 1,
      "welcomeImageUrl": {},
      "welcomeSubject": {},
      "welcomeText": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeUntil` | object |  |
| `applicationFormAgreement` | object |  |
| `applicationFormBenefits` | object |  |
| `applicationFormFooter` | object |  |
| `applicationFormHeader` | object |  |
| `applicationFormIsAddressEnabled` | boolean |  |
| `applicationFormIsBirthDateEnabled` | boolean |  |
| `applicationFormIsBirthPlaceEnabled` | boolean |  |
| `applicationFormIsCommentsEnabled` | boolean |  |
| `applicationFormIsGenderEnabled` | boolean |  |
| `applicationFormIsNationalityEnabled` | boolean |  |
| `applicationFormIsTaxNumberEnabled` | boolean |  |
| `applicationFormIsUnder18ControlEnabled` | boolean |  |
| `applicationFormRegistrationFee` | number |  |
| `applicationFormTitle` | object |  |
| `balance` | number |  |
| `commissionFee` | number |  |
| `commissionFeeCurrency` | number |  |
| `commissionRate` | number |  |
| `createdOn` | string |  |
| `creditCardProcessor` | number |  |
| `currency` | number |  |
| `defaultAddressCountry` | string |  |
| `defaultEmailIdentityId` | string |  |
| `defaultPhoneCountryCode` | string |  |
| `defaultSmsIdentityId` | string |  |
| `googleAnalyticsTrackerId` | object |  |
| `id` | string |  |
| `invoiceAddress` | object |  |
| `isApplicationFormEnabled` | boolean |  |
| `isCityListVisible` | boolean |  |
| `isCompanyListVisible` | boolean |  |
| `isCountryListVisible` | boolean |  |
| `isCustomPaymentEnabled` | boolean |  |
| `isDeleted` | boolean |  |
| `isDonationEnabled` | boolean |  |
| `isJobPostingsEnabled` | boolean |  |
| `isLoginPasswordEnabled` | boolean |  |
| `isLoginSmsEnabled` | boolean |  |
| `isLoginSocialNetworkEnabled` | boolean |  |
| `isLoginTwoFactorEnabled` | boolean |  |
| `isLoginWithOneTimeLoginEnabled` | boolean |  |
| `isMemberListVisible` | boolean |  |
| `isOfferedServicesEnabled` | boolean |  |
| `isOnlineCreditCardEnabled` | boolean |  |
| `isPaymentEnabled` | boolean |  |
| `isSchoolListVisible` | boolean |  |
| `isSectorListVisible` | boolean |  |
| `isTermsOfUseRequiredForAccess` | boolean |  |
| `isWeeklyNewsletterAnnouncements` | boolean |  |
| `isWeeklyNewsletterDonationCampaigns` | boolean |  |
| `isWeeklyNewsletterEnabled` | boolean |  |
| `isWeeklyNewsletterJobOffers` | boolean |  |
| `isWeeklyNewsletterJobSeekers` | boolean |  |
| `isWeeklyNewsletterMemberDebt` | boolean |  |
| `isWeeklyNewsletterMemberUnreadMessages` | boolean |  |
| `isWeeklyNewsletterNewMembersEnabled` | boolean |  |
| `isWeeklyNewsletterServices` | boolean |  |
| `language` | string |  |
| `legalEntityOwnersVerificationDocumentUrl` | object |  |
| `legalEntityVerificationDocumentUrl` | object |  |
| `loginPageTitle` | object |  |
| `logoHeight` | number |  |
| `logoUrl` | string |  |
| `logoWidth` | number |  |
| `memberNoType` | number |  |
| `membershipTerms` | object |  |
| `name` | string |  |
| `onlineCreditCardSubMerchantId` | object |  |
| `organisationColor1` | string |  |
| `organisationColor2` | object |  |
| `organisationSupportEmail` | string |  |
| `organisationSupportPhone` | string |  |
| `paymentFooter` | object |  |
| `paymentHeader` | object |  |
| `permalink` | string |  |
| `shortName` | string |  |
| `smsIsEnabled` | boolean |  |
| `smsProfit` | number |  |
| `state` | number |  |
| `stripeCustomerId` | string |  |
| `stripePlanId` | object |  |
| `termsOfUse2App` | object |  |
| `termsOfUseApp` | object |  |
| `timeZoneId` | string |  |
| `totalCost` | number |  |
| `totalProfit` | number |  |
| `welcomeImageUrl` | object |  |
| `welcomeSubject` | object |  |
| `welcomeText` | object |  |

## Native endpoint

Through the native Raklet API, this operation is `GET /app/organisations/:organisationId/settings` (base URL `https://api.raklet.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organisation-settings.md) for the provider-specific parameters and requirements.

