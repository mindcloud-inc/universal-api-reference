# Outseta: Register Account

Registers an account in Outseta.

```
POST https://connect.mindcloud.co/v1/universal/outseta/latest/actions/register-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Outseta `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/outseta/latest/actions/register-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/outseta/latest/actions/register-account', {
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
| `name` | string | no |  |
| `personAccount[].isPrimary` | boolean | no |  |
| `personAccount[].person.email` | string | no |  |
| `subscriptions[].billingRenewalTerm` | number | no |  |
| `subscriptions[].plan.uid` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_objectType": "string",
      "AccountSpecificPageUrl1": "https://example.com",
      "AccountSpecificPageUrl10": "https://example.com",
      "AccountSpecificPageUrl2": "https://example.com",
      "AccountSpecificPageUrl3": "https://example.com",
      "AccountSpecificPageUrl4": "https://example.com",
      "AccountSpecificPageUrl5": "https://example.com",
      "AccountSpecificPageUrl6": "https://example.com",
      "AccountSpecificPageUrl7": "https://example.com",
      "AccountSpecificPageUrl8": "https://example.com",
      "AccountSpecificPageUrl9": "https://example.com",
      "AccountStage": 1,
      "AccountStageLabel": "string",
      "ActivityEventData": "string",
      "BillingAddress": "string",
      "ClientIdentifier": "string",
      "Created": "string",
      "CurrentSubscription": {
        "_objectType": "string",
        "Account": "string",
        "ActivityEventData": "string",
        "BillingRenewalTerm": 1,
        "Created": "string",
        "DiscountCode": "string",
        "DiscountCouponSubscriptions": "string",
        "EndDate": "string",
        "ExpirationDate": "string",
        "IsPlanUpgradeRequired": true,
        "LatestInvoice": "string",
        "NewRequiredQuantity": "string",
        "Plan": "string",
        "PlanUpgradeRequiredMessage": "string",
        "Quantity": "string",
        "Rate": 1,
        "RenewalDate": "string",
        "StartDate": "string",
        "SubscriptionAddOns": "string",
        "Uid": "string",
        "Updated": "string"
      },
      "Deals": [
        "string"
      ],
      "DomainName": "Ava Chen",
      "HasLoggedIn": true,
      "InvoiceNotes": "string",
      "IsDemo": true,
      "LastLoginDateTime": "string",
      "LatestSubscription": {
        "_objectType": "string",
        "Account": "string",
        "ActivityEventData": "string",
        "BillingRenewalTerm": 1,
        "Created": "string",
        "DiscountCode": "string",
        "DiscountCouponSubscriptions": "string",
        "EndDate": "string",
        "ExpirationDate": "string",
        "IsPlanUpgradeRequired": true,
        "LatestInvoice": "string",
        "NewRequiredQuantity": "string",
        "Plan": "string",
        "PlanUpgradeRequiredMessage": "string",
        "Quantity": "string",
        "Rate": 1,
        "RenewalDate": "string",
        "StartDate": "string",
        "SubscriptionAddOns": "string",
        "Uid": "string",
        "Updated": "string"
      },
      "LifetimeRevenue": 1,
      "MailingAddress": "string",
      "Name": "Ava Chen",
      "PaymentInformation": "string",
      "PersonAccount": [
        {
          "_objectType": "string",
          "Account": "string",
          "ActivityEventData": "string",
          "Created": "string",
          "IsPrimary": true,
          "Person": "string",
          "Uid": "string",
          "Updated": "string"
        }
      ],
      "PrimaryContact": {
        "_objectType": "string",
        "Account": "string",
        "AccountUids": "string",
        "ActivityEventData": "string",
        "Created": "string",
        "DealPeople": "string",
        "DiscordUser": "string",
        "Email": "ava@example.com",
        "EmailListPerson": "ava@example.com",
        "FirstName": "Ava",
        "FullName": "Ava Chen",
        "HasLoggedIn": true,
        "HasUnsubscribed": true,
        "IPAddress": "string",
        "IsConnectedToDiscord": true,
        "Language": "string",
        "LastLoginDateTime": "string",
        "LastName": "Chen",
        "LeadFormSubmissions": "string",
        "MailingAddress": "string",
        "OAuthGoogleProfileId": "string",
        "OAuthIntegrationStatus": 1,
        "PasswordLastUpdated": "string",
        "PasswordMustChange": true,
        "PersonAccount": "string",
        "PhoneMobile": "string",
        "PhoneWork": "string",
        "ProfileImageS3Url": "https://example.com",
        "Referer": "string",
        "Timezone": "string",
        "Title": "string",
        "Uid": "string",
        "Updated": "string",
        "UserAgent": "string",
        "UserAgentPlatformBrowser": "string"
      },
      "PrimarySubscription": "string",
      "RecaptchaToken": "string",
      "RewardFulReferralId": "string",
      "Subscriptions": [
        {
          "_objectType": "string",
          "Account": "string",
          "ActivityEventData": "string",
          "BillingRenewalTerm": 1,
          "Created": "string",
          "DiscountCode": "string",
          "DiscountCouponSubscriptions": "string",
          "EndDate": "string",
          "ExpirationDate": "string",
          "IsPlanUpgradeRequired": true,
          "LatestInvoice": "string",
          "NewRequiredQuantity": "string",
          "Plan": "string",
          "PlanUpgradeRequiredMessage": "string",
          "Quantity": "string",
          "Rate": 1,
          "RenewalDate": "string",
          "StartDate": "string",
          "SubscriptionAddOns": "string",
          "Uid": "string",
          "Updated": "string"
        }
      ],
      "Uid": "string",
      "Updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_objectType` | string |  |
| `AccountSpecificPageUrl1` | string |  |
| `AccountSpecificPageUrl10` | string |  |
| `AccountSpecificPageUrl2` | string |  |
| `AccountSpecificPageUrl3` | string |  |
| `AccountSpecificPageUrl4` | string |  |
| `AccountSpecificPageUrl5` | string |  |
| `AccountSpecificPageUrl6` | string |  |
| `AccountSpecificPageUrl7` | string |  |
| `AccountSpecificPageUrl8` | string |  |
| `AccountSpecificPageUrl9` | string |  |
| `AccountStage` | number |  |
| `AccountStageLabel` | string |  |
| `ActivityEventData` | string |  |
| `BillingAddress` | string |  |
| `ClientIdentifier` | string |  |
| `Created` | string |  |
| `CurrentSubscription._objectType` | string |  |
| `CurrentSubscription.Account` | string |  |
| `CurrentSubscription.ActivityEventData` | string |  |
| `CurrentSubscription.BillingRenewalTerm` | number |  |
| `CurrentSubscription.Created` | string |  |
| `CurrentSubscription.DiscountCode` | string |  |
| `CurrentSubscription.DiscountCouponSubscriptions` | string |  |
| `CurrentSubscription.EndDate` | string |  |
| `CurrentSubscription.ExpirationDate` | string |  |
| `CurrentSubscription.IsPlanUpgradeRequired` | boolean |  |
| `CurrentSubscription.LatestInvoice` | string |  |
| `CurrentSubscription.NewRequiredQuantity` | string |  |
| `CurrentSubscription.Plan` | string |  |
| `CurrentSubscription.PlanUpgradeRequiredMessage` | string |  |
| `CurrentSubscription.Quantity` | string |  |
| `CurrentSubscription.Rate` | number |  |
| `CurrentSubscription.RenewalDate` | string |  |
| `CurrentSubscription.StartDate` | string |  |
| `CurrentSubscription.SubscriptionAddOns` | string |  |
| `CurrentSubscription.Uid` | string |  |
| `CurrentSubscription.Updated` | string |  |
| `Deals` | array<string> |  |
| `DomainName` | string |  |
| `HasLoggedIn` | boolean |  |
| `InvoiceNotes` | string |  |
| `IsDemo` | boolean |  |
| `LastLoginDateTime` | string |  |
| `LatestSubscription._objectType` | string |  |
| `LatestSubscription.Account` | string |  |
| `LatestSubscription.ActivityEventData` | string |  |
| `LatestSubscription.BillingRenewalTerm` | number |  |
| `LatestSubscription.Created` | string |  |
| `LatestSubscription.DiscountCode` | string |  |
| `LatestSubscription.DiscountCouponSubscriptions` | string |  |
| `LatestSubscription.EndDate` | string |  |
| `LatestSubscription.ExpirationDate` | string |  |
| `LatestSubscription.IsPlanUpgradeRequired` | boolean |  |
| `LatestSubscription.LatestInvoice` | string |  |
| `LatestSubscription.NewRequiredQuantity` | string |  |
| `LatestSubscription.Plan` | string |  |
| `LatestSubscription.PlanUpgradeRequiredMessage` | string |  |
| `LatestSubscription.Quantity` | string |  |
| `LatestSubscription.Rate` | number |  |
| `LatestSubscription.RenewalDate` | string |  |
| `LatestSubscription.StartDate` | string |  |
| `LatestSubscription.SubscriptionAddOns` | string |  |
| `LatestSubscription.Uid` | string |  |
| `LatestSubscription.Updated` | string |  |
| `LifetimeRevenue` | number |  |
| `MailingAddress` | string |  |
| `Name` | string |  |
| `PaymentInformation` | string |  |
| `PersonAccount` | array<object> |  |
| `PersonAccount[]._objectType` | string |  |
| `PersonAccount[].Account` | string |  |
| `PersonAccount[].ActivityEventData` | string |  |
| `PersonAccount[].Created` | string |  |
| `PersonAccount[].IsPrimary` | boolean |  |
| `PersonAccount[].Person` | string |  |
| `PersonAccount[].Uid` | string |  |
| `PersonAccount[].Updated` | string |  |
| `PrimaryContact._objectType` | string |  |
| `PrimaryContact.Account` | string |  |
| `PrimaryContact.AccountUids` | string |  |
| `PrimaryContact.ActivityEventData` | string |  |
| `PrimaryContact.Created` | string |  |
| `PrimaryContact.DealPeople` | string |  |
| `PrimaryContact.DiscordUser` | string |  |
| `PrimaryContact.Email` | string |  |
| `PrimaryContact.EmailListPerson` | string |  |
| `PrimaryContact.FirstName` | string |  |
| `PrimaryContact.FullName` | string |  |
| `PrimaryContact.HasLoggedIn` | boolean |  |
| `PrimaryContact.HasUnsubscribed` | boolean |  |
| `PrimaryContact.IPAddress` | string |  |
| `PrimaryContact.IsConnectedToDiscord` | boolean |  |
| `PrimaryContact.Language` | string |  |
| `PrimaryContact.LastLoginDateTime` | string |  |
| `PrimaryContact.LastName` | string |  |
| `PrimaryContact.LeadFormSubmissions` | string |  |
| `PrimaryContact.MailingAddress` | string |  |
| `PrimaryContact.OAuthGoogleProfileId` | string |  |
| `PrimaryContact.OAuthIntegrationStatus` | number |  |
| `PrimaryContact.PasswordLastUpdated` | string |  |
| `PrimaryContact.PasswordMustChange` | boolean |  |
| `PrimaryContact.PersonAccount` | string |  |
| `PrimaryContact.PhoneMobile` | string |  |
| `PrimaryContact.PhoneWork` | string |  |
| `PrimaryContact.ProfileImageS3Url` | string |  |
| `PrimaryContact.Referer` | string |  |
| `PrimaryContact.Timezone` | string |  |
| `PrimaryContact.Title` | string |  |
| `PrimaryContact.Uid` | string |  |
| `PrimaryContact.Updated` | string |  |
| `PrimaryContact.UserAgent` | string |  |
| `PrimaryContact.UserAgentPlatformBrowser` | string |  |
| `PrimarySubscription` | string |  |
| `RecaptchaToken` | string |  |
| `RewardFulReferralId` | string |  |
| `Subscriptions` | array<object> |  |
| `Subscriptions[]._objectType` | string |  |
| `Subscriptions[].Account` | string |  |
| `Subscriptions[].ActivityEventData` | string |  |
| `Subscriptions[].BillingRenewalTerm` | number |  |
| `Subscriptions[].Created` | string |  |
| `Subscriptions[].DiscountCode` | string |  |
| `Subscriptions[].DiscountCouponSubscriptions` | string |  |
| `Subscriptions[].EndDate` | string |  |
| `Subscriptions[].ExpirationDate` | string |  |
| `Subscriptions[].IsPlanUpgradeRequired` | boolean |  |
| `Subscriptions[].LatestInvoice` | string |  |
| `Subscriptions[].NewRequiredQuantity` | string |  |
| `Subscriptions[].Plan` | string |  |
| `Subscriptions[].PlanUpgradeRequiredMessage` | string |  |
| `Subscriptions[].Quantity` | string |  |
| `Subscriptions[].Rate` | number |  |
| `Subscriptions[].RenewalDate` | string |  |
| `Subscriptions[].StartDate` | string |  |
| `Subscriptions[].SubscriptionAddOns` | string |  |
| `Subscriptions[].Uid` | string |  |
| `Subscriptions[].Updated` | string |  |
| `Uid` | string |  |
| `Updated` | string |  |

## Native endpoint

Through the native Outseta API, this operation is `POST /crm/registrations` (base URL `https://{{credentials.subdomain}}.outseta.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/register-account.md) for the provider-specific parameters and requirements.

