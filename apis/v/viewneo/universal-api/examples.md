# Viewneo Universal API Examples

These examples use the MindCloud API key and Viewneo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account

Retrieves the current account details from Viewneo.

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

Example response:

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

See the full [Get Account action reference](actions/get-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/viewneo/latest/actions/get-account).

## Copy Multiple Media Files

Copies multiple media files in Viewneo.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/viewneo/latest/actions/copy-multiple-media-files" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "targetId": 1,
  "mediaFileIds[]": [
    1
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viewneo/latest/actions/copy-multiple-media-files', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "targetId": 1,
    "mediaFileIds[]": [1]
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Copy Multiple Media Files action reference](actions/copy-multiple-media-files.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/viewneo/latest/actions/copy-multiple-media-files).
