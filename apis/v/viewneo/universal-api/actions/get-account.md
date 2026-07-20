# Viewneo: Get Account

Retrieves the current account details from Viewneo.

```
GET https://connect.mindcloud.co/v1/universal/viewneo/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewneo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/viewneo/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/viewneo/latest/actions/get-account?${params}`, {
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
      "cameraCount": 1,
      "company": {
        "alltronReseller": {},
        "branch": 1,
        "brandCompanyId": {},
        "city": "string",
        "country": "string",
        "createdAt": "string",
        "customDunning": 1,
        "customLicencePrice": {},
        "deletedAt": {},
        "deletesAt": {},
        "description": {},
        "discountValue": {},
        "expiresAt": {},
        "geoLocation": "string",
        "id": 1,
        "isAnalyticsEnabled": {},
        "isBrand": 1,
        "isDiniopayEnabled": 1,
        "isLocked": 1,
        "isPartner": 1,
        "isTrial": 1,
        "lastLoginAt": "string",
        "maxAmountCustomLicencePrice": {},
        "microsoftFaceApiKey": {},
        "microsoftFaceApiUrl": {},
        "name": "Ava Chen",
        "parentId": {},
        "partner": {},
        "partnerId": {},
        "postalCode": "string",
        "priceAdjustment": 1,
        "registrationType": 1,
        "stage": {},
        "state": "string",
        "street": "string",
        "streetNumber": "string",
        "stripeCustomerId": {},
        "subName": "Ava Chen",
        "totalLicences": "string",
        "totalStorage": {},
        "totalSubAccounts": 1,
        "type": 1,
        "updatedAt": "string",
        "userIdAsPartner": {},
        "vat": "string"
      },
      "coupon": {},
      "currency": "string",
      "defaultPlaylist": {},
      "dinioCount": 1,
      "diwaCount": 1,
      "isAnalyticsEnabled": {},
      "isPremiumPartner": true,
      "isSubAccount": true,
      "isWhitelabeled": true,
      "numberOfDevices": 1,
      "numberOfLicences": 1,
      "numberOfUnusedLicences": 1,
      "rfidHubCount": 1,
      "subscription": {
        "cancelAt": {},
        "companyId": 1,
        "count": 1,
        "createdAt": "string",
        "currency": "string",
        "deletedAt": {},
        "expireAt": "string",
        "Id": "string",
        "interval": "string",
        "items": [
          {
            "addToPayment": true,
            "Id": "string",
            "plan": {
              "Id": "string",
              "isHidden": true,
              "isMulti": true,
              "label": "string",
              "name": "Ava Chen",
              "priceMonthly": {
                "eur": 1,
                "Id": "string",
                "usd": 1
              },
              "priceYearly": {
                "eur": 1,
                "Id": "string",
                "usd": 1
              },
              "V": 1,
              "version": 1,
              "zohoItemId": "string"
            },
            "startedAt": "string"
          }
        ],
        "minCount": {},
        "setup": true,
        "startedAt": "string",
        "status": "string",
        "updatedAt": "string",
        "V": 1
      },
      "taxPercent": 1,
      "taxPercentAnnual": 1,
      "totalCredit": 1,
      "totalStorage": 1,
      "usedStorage": 1,
      "user": {
        "companyId": 1,
        "confirmationCode": {},
        "createdAt": "string",
        "deletedAt": {},
        "displayLanguage": "string",
        "email": "ava@example.com",
        "emailChangeRequestedAt": {},
        "emailToChange": {},
        "errorCounter": 1,
        "fax": {},
        "firstname": "Ava",
        "id": 1,
        "isAffiliateEmail": 1,
        "isBlocked": 1,
        "isNewsletterSubscribed": 1,
        "lastLoginAttemptAt": {},
        "lastname": "Chen",
        "loggedInAt": "string",
        "mobile": {},
        "mqttSettings": {
          "host": "string",
          "port": "string",
          "protocol": "string",
          "token": "string",
          "username": "Ava Chen"
        },
        "phone": {},
        "qrToken": {},
        "salutation": "string",
        "tfaActivatedAt": {},
        "tfaEmail": {},
        "tfaSecretKey": {},
        "updatedAt": "string",
        "userGroup": {
          "companyId": {},
          "createdAt": "string",
          "deletedAt": {},
          "description": {},
          "id": 1,
          "name": "Ava Chen",
          "pivot": {
            "userGroupId": 1,
            "userId": 1
          },
          "type": 1,
          "updatedAt": "string"
        },
        "userGroupId": 1,
        "userGroups": [
          {
            "companyId": {},
            "createdAt": "string",
            "deletedAt": {},
            "description": {},
            "id": 1,
            "name": "Ava Chen",
            "permittedFeatures": [
              {
                "action": "string",
                "companyId": {},
                "createdAt": "string",
                "deletedAt": {},
                "id": 1,
                "isPermitted": 1,
                "resourceId": {},
                "resourceType": "string",
                "scopeId": {},
                "scopeType": {},
                "senderId": {},
                "updatedAt": "string",
                "userGroupId": 1,
                "userId": {}
              }
            ],
            "pivot": {
              "userGroupId": 1,
              "userId": 1
            },
            "type": 1,
            "updatedAt": "string"
          }
        ],
        "verifiedAt": "string",
        "zohoCrmContactId": {},
        "zohoCrmLeadId": {}
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cameraCount` | number |  |
| `company.alltronReseller` | object |  |
| `company.branch` | number |  |
| `company.brandCompanyId` | object |  |
| `company.city` | string |  |
| `company.country` | string |  |
| `company.createdAt` | string |  |
| `company.customDunning` | number |  |
| `company.customLicencePrice` | object |  |
| `company.deletedAt` | object |  |
| `company.deletesAt` | object |  |
| `company.description` | object |  |
| `company.discountValue` | object |  |
| `company.expiresAt` | object |  |
| `company.geoLocation` | string |  |
| `company.id` | number |  |
| `company.isAnalyticsEnabled` | object |  |
| `company.isBrand` | number |  |
| `company.isDiniopayEnabled` | number |  |
| `company.isLocked` | number |  |
| `company.isPartner` | number |  |
| `company.isTrial` | number |  |
| `company.lastLoginAt` | string |  |
| `company.maxAmountCustomLicencePrice` | object |  |
| `company.microsoftFaceApiKey` | object |  |
| `company.microsoftFaceApiUrl` | object |  |
| `company.name` | string |  |
| `company.parentId` | object |  |
| `company.partner` | object |  |
| `company.partnerId` | object |  |
| `company.postalCode` | string |  |
| `company.priceAdjustment` | number |  |
| `company.registrationType` | number |  |
| `company.stage` | object |  |
| `company.state` | string |  |
| `company.street` | string |  |
| `company.streetNumber` | string |  |
| `company.stripeCustomerId` | object |  |
| `company.subName` | string |  |
| `company.totalLicences` | string |  |
| `company.totalStorage` | object |  |
| `company.totalSubAccounts` | number |  |
| `company.type` | number |  |
| `company.updatedAt` | string |  |
| `company.userIdAsPartner` | object |  |
| `company.vat` | string |  |
| `coupon` | object |  |
| `currency` | string |  |
| `defaultPlaylist` | object |  |
| `dinioCount` | number |  |
| `diwaCount` | number |  |
| `isAnalyticsEnabled` | object |  |
| `isPremiumPartner` | boolean |  |
| `isSubAccount` | boolean |  |
| `isWhitelabeled` | boolean |  |
| `numberOfDevices` | number |  |
| `numberOfLicences` | number |  |
| `numberOfUnusedLicences` | number |  |
| `rfidHubCount` | number |  |
| `subscription.cancelAt` | object |  |
| `subscription.companyId` | number |  |
| `subscription.count` | number |  |
| `subscription.createdAt` | string |  |
| `subscription.currency` | string |  |
| `subscription.deletedAt` | object |  |
| `subscription.expireAt` | string |  |
| `subscription.Id` | string |  |
| `subscription.interval` | string |  |
| `subscription.items[].addToPayment` | boolean |  |
| `subscription.items[].Id` | string |  |
| `subscription.items[].plan.Id` | string |  |
| `subscription.items[].plan.isHidden` | boolean |  |
| `subscription.items[].plan.isMulti` | boolean |  |
| `subscription.items[].plan.label` | string |  |
| `subscription.items[].plan.name` | string |  |
| `subscription.items[].plan.priceMonthly.eur` | number |  |
| `subscription.items[].plan.priceMonthly.Id` | string |  |
| `subscription.items[].plan.priceMonthly.usd` | number |  |
| `subscription.items[].plan.priceYearly.eur` | number |  |
| `subscription.items[].plan.priceYearly.Id` | string |  |
| `subscription.items[].plan.priceYearly.usd` | number |  |
| `subscription.items[].plan.V` | number |  |
| `subscription.items[].plan.version` | number |  |
| `subscription.items[].plan.zohoItemId` | string |  |
| `subscription.items[].startedAt` | string |  |
| `subscription.minCount` | object |  |
| `subscription.setup` | boolean |  |
| `subscription.startedAt` | string |  |
| `subscription.status` | string |  |
| `subscription.updatedAt` | string |  |
| `subscription.V` | number |  |
| `taxPercent` | number |  |
| `taxPercentAnnual` | number |  |
| `totalCredit` | number |  |
| `totalStorage` | number |  |
| `usedStorage` | number |  |
| `user.companyId` | number |  |
| `user.confirmationCode` | object |  |
| `user.createdAt` | string |  |
| `user.deletedAt` | object |  |
| `user.displayLanguage` | string |  |
| `user.email` | string |  |
| `user.emailChangeRequestedAt` | object |  |
| `user.emailToChange` | object |  |
| `user.errorCounter` | number |  |
| `user.fax` | object |  |
| `user.firstname` | string |  |
| `user.id` | number |  |
| `user.isAffiliateEmail` | number |  |
| `user.isBlocked` | number |  |
| `user.isNewsletterSubscribed` | number |  |
| `user.lastLoginAttemptAt` | object |  |
| `user.lastname` | string |  |
| `user.loggedInAt` | string |  |
| `user.mobile` | object |  |
| `user.mqttSettings.host` | string |  |
| `user.mqttSettings.port` | string |  |
| `user.mqttSettings.protocol` | string |  |
| `user.mqttSettings.token` | string |  |
| `user.mqttSettings.username` | string |  |
| `user.phone` | object |  |
| `user.qrToken` | object |  |
| `user.salutation` | string |  |
| `user.tfaActivatedAt` | object |  |
| `user.tfaEmail` | object |  |
| `user.tfaSecretKey` | object |  |
| `user.updatedAt` | string |  |
| `user.userGroup.companyId` | object |  |
| `user.userGroup.createdAt` | string |  |
| `user.userGroup.deletedAt` | object |  |
| `user.userGroup.description` | object |  |
| `user.userGroup.id` | number |  |
| `user.userGroup.name` | string |  |
| `user.userGroup.pivot.userGroupId` | number |  |
| `user.userGroup.pivot.userId` | number |  |
| `user.userGroup.type` | number |  |
| `user.userGroup.updatedAt` | string |  |
| `user.userGroupId` | number |  |
| `user.userGroups[].companyId` | object |  |
| `user.userGroups[].createdAt` | string |  |
| `user.userGroups[].deletedAt` | object |  |
| `user.userGroups[].description` | object |  |
| `user.userGroups[].id` | number |  |
| `user.userGroups[].name` | string |  |
| `user.userGroups[].permittedFeatures[].action` | string |  |
| `user.userGroups[].permittedFeatures[].companyId` | object |  |
| `user.userGroups[].permittedFeatures[].createdAt` | string |  |
| `user.userGroups[].permittedFeatures[].deletedAt` | object |  |
| `user.userGroups[].permittedFeatures[].id` | number |  |
| `user.userGroups[].permittedFeatures[].isPermitted` | number |  |
| `user.userGroups[].permittedFeatures[].resourceId` | object |  |
| `user.userGroups[].permittedFeatures[].resourceType` | string |  |
| `user.userGroups[].permittedFeatures[].scopeId` | object |  |
| `user.userGroups[].permittedFeatures[].scopeType` | object |  |
| `user.userGroups[].permittedFeatures[].senderId` | object |  |
| `user.userGroups[].permittedFeatures[].updatedAt` | string |  |
| `user.userGroups[].permittedFeatures[].userGroupId` | number |  |
| `user.userGroups[].permittedFeatures[].userId` | object |  |
| `user.userGroups[].pivot.userGroupId` | number |  |
| `user.userGroups[].pivot.userId` | number |  |
| `user.userGroups[].type` | number |  |
| `user.userGroups[].updatedAt` | string |  |
| `user.verifiedAt` | string |  |
| `user.zohoCrmContactId` | object |  |
| `user.zohoCrmLeadId` | object |  |

## Native endpoint

Through the native Viewneo API, this operation is `GET /account` (base URL `https://cloud.viewneo.com/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.

