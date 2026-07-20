# Raklet Universal API Examples

These examples use the MindCloud API key and Raklet connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get organisation settings



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

Example response:

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

See the full [Get organisation settings action reference](actions/get-organisation-settings.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/raklet/latest/actions/get-organisation-settings).

## Add Contact Address



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/raklet/latest/actions/add-contact-address" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organisationMembershipId": "string",
  "details": "string",
  "city": "string",
  "country": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/raklet/latest/actions/add-contact-address', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organisationMembershipId": "string",
    "details": "string",
    "city": "string",
    "country": "string"
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
      "code": 1,
      "data": {
        "city": "string",
        "country": "string",
        "county": "string",
        "details": "string",
        "fullAddress": "string",
        "id": "string",
        "postalCode": "string",
        "state": "string"
      },
      "errors": [
        {}
      ],
      "isSuccess": true
    }
  ],
  "meta": {}
}
```

See the full [Add Contact Address action reference](actions/add-contact-address.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/raklet/latest/actions/add-contact-address).
