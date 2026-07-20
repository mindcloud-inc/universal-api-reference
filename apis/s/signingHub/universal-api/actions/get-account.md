# SigningHub: Get Account

Retrieves account details from SigningHub.

```
GET https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SigningHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/get-account?${params}`, {
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
      "billing": {
        "billingInformation": true,
        "billingStatus": "string",
        "currency": {},
        "duration": "string",
        "emailAddress": "ava@example.com",
        "mobileNumber": "string",
        "nextBillingDate": "string",
        "price": "string",
        "provider": "string",
        "userName": "Ava Chen"
      },
      "companyName": "Ava Chen",
      "country": "string",
      "createdOn": "string",
      "displayPlanUpgradeBanner": true,
      "enabled": true,
      "enterprise": {
        "enterpriseId": 1,
        "enterpriseName": "Ava Chen",
        "enterpriseUrl": "https://example.com",
        "errorNotificationTimeout": 1,
        "mobileNumber": "string",
        "owner": "string",
        "ownerEmail": "ava@example.com",
        "supportEmail": {},
        "workspaceId": {}
      },
      "fonts": [
        {
          "name": "Ava Chen"
        }
      ],
      "jobTitle": "string",
      "language": "string",
      "lastLogin": "string",
      "mobileNumber": "string",
      "servicePlan": {
        "addUniqueIdentifier": true,
        "appearanceDesign": {
          "selected": [
            {
              "designName": "Ava Chen",
              "designPreview": "string",
              "designPreviewUrl": "https://example.com"
            }
          ]
        },
        "billing": {
          "mode": "string",
          "nextBillingDate": "string",
          "paymentType": "string",
          "price": "string",
          "yearlyPrice": "string"
        },
        "constraints": {
          "advancedElectronicSeals": "string",
          "advancedElectronicSignatures": "string",
          "electronicSeals": "string",
          "highTrustAdvancedSignatures": "string",
          "maxUploadSize": "string",
          "qualifiedElectronicSeals": "string",
          "qualifiedElectronicSignatures": "string",
          "signatures": "string",
          "simpleElectronicSignatures": {},
          "storage": "string",
          "templates": "string",
          "users": "string",
          "workflows": "string"
        },
        "csp": {
          "enabled": true
        },
        "deprecated": true,
        "endDate": {},
        "features": [
          "string"
        ],
        "fonts": [
          {
            "name": "Ava Chen"
          }
        ],
        "id": 1,
        "name": "Ava Chen",
        "ras": {
          "clientId": "string",
          "clientSecret": "string",
          "url": "https://example.com"
        },
        "settings": {
          "authorizedSigning": true,
          "autoArchiving": true,
          "autoDeletion": true,
          "certifyOptions": {
            "default": "string",
            "selected": [
              "string"
            ]
          },
          "emailOtp": true,
          "pdfCompliant": true,
          "readonlyUserFields": {},
          "signatureType": "string",
          "signingKeysWithPassword": true,
          "smsNotification": true,
          "smsOtp": true,
          "smsOtpLength": 1,
          "smsOtpRetryDuration": 1,
          "totp": true,
          "workflowEvidence": "string"
        },
        "signaturePad": {
          "enabled": true,
          "server": {}
        },
        "signatureSettings": {
          "levelOfAssurance": {
            "selected": [
              "string"
            ]
          },
          "signingServers": [
            {
              "capacity": {
                "advancedElectronicSeal": {
                  "enabled": true
                },
                "advancedElectronicSignature": {
                  "enabled": true,
                  "selected": [
                    {
                      "id": 1,
                      "keyProtection": "string",
                      "levelOfAssurance": "string",
                      "name": "Ava Chen"
                    }
                  ]
                },
                "electronicSeal": {
                  "enabled": true,
                  "selected": [
                    {
                      "id": 1,
                      "keyProtection": "string",
                      "levelOfAssurance": "string",
                      "name": "Ava Chen"
                    }
                  ]
                },
                "highTrustAdvanced": {
                  "enabled": true
                },
                "qualifiedElectronicSeal": {
                  "enabled": true
                },
                "qualifiedElectronicSignature": {
                  "enabled": true
                }
              },
              "info": {
                "appearanceDesignName": {},
                "appearanceLogo": {},
                "authType": {},
                "id": 1,
                "keyLocation": "string",
                "levelOfAssurance": {},
                "name": "Ava Chen",
                "order": {},
                "provider": "string",
                "signatureType": [
                  "string"
                ]
              }
            }
          ]
        },
        "startDate": "string",
        "type": "string"
      },
      "timeZone": "string",
      "twoFactorAuthenticationEnabled": true,
      "userEmail": "ava@example.com",
      "userId": 1,
      "userName": "Ava Chen",
      "userNationalId": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billing.billingInformation` | boolean |  |
| `billing.billingStatus` | string |  |
| `billing.currency` | object |  |
| `billing.duration` | string |  |
| `billing.emailAddress` | string |  |
| `billing.mobileNumber` | string |  |
| `billing.nextBillingDate` | string |  |
| `billing.price` | string |  |
| `billing.provider` | string |  |
| `billing.userName` | string |  |
| `companyName` | string |  |
| `country` | string |  |
| `createdOn` | string |  |
| `displayPlanUpgradeBanner` | boolean |  |
| `enabled` | boolean |  |
| `enterprise.enterpriseId` | number |  |
| `enterprise.enterpriseName` | string |  |
| `enterprise.enterpriseUrl` | string |  |
| `enterprise.errorNotificationTimeout` | number |  |
| `enterprise.mobileNumber` | string |  |
| `enterprise.owner` | string |  |
| `enterprise.ownerEmail` | string |  |
| `enterprise.supportEmail` | object |  |
| `enterprise.workspaceId` | object |  |
| `fonts[].name` | string |  |
| `jobTitle` | string |  |
| `language` | string |  |
| `lastLogin` | string |  |
| `mobileNumber` | string |  |
| `servicePlan.addUniqueIdentifier` | boolean |  |
| `servicePlan.appearanceDesign.selected[].designName` | string |  |
| `servicePlan.appearanceDesign.selected[].designPreview` | string |  |
| `servicePlan.appearanceDesign.selected[].designPreviewUrl` | string |  |
| `servicePlan.billing.mode` | string |  |
| `servicePlan.billing.nextBillingDate` | string |  |
| `servicePlan.billing.paymentType` | string |  |
| `servicePlan.billing.price` | string |  |
| `servicePlan.billing.yearlyPrice` | string |  |
| `servicePlan.constraints.advancedElectronicSeals` | string |  |
| `servicePlan.constraints.advancedElectronicSignatures` | string |  |
| `servicePlan.constraints.electronicSeals` | string |  |
| `servicePlan.constraints.highTrustAdvancedSignatures` | string |  |
| `servicePlan.constraints.maxUploadSize` | string |  |
| `servicePlan.constraints.qualifiedElectronicSeals` | string |  |
| `servicePlan.constraints.qualifiedElectronicSignatures` | string |  |
| `servicePlan.constraints.signatures` | string |  |
| `servicePlan.constraints.simpleElectronicSignatures` | object |  |
| `servicePlan.constraints.storage` | string |  |
| `servicePlan.constraints.templates` | string |  |
| `servicePlan.constraints.users` | string |  |
| `servicePlan.constraints.workflows` | string |  |
| `servicePlan.csp.enabled` | boolean |  |
| `servicePlan.deprecated` | boolean |  |
| `servicePlan.endDate` | object |  |
| `servicePlan.features[]` | string |  |
| `servicePlan.fonts[].name` | string |  |
| `servicePlan.id` | number |  |
| `servicePlan.name` | string |  |
| `servicePlan.ras.clientId` | string |  |
| `servicePlan.ras.clientSecret` | string |  |
| `servicePlan.ras.url` | string |  |
| `servicePlan.settings.authorizedSigning` | boolean |  |
| `servicePlan.settings.autoArchiving` | boolean |  |
| `servicePlan.settings.autoDeletion` | boolean |  |
| `servicePlan.settings.certifyOptions.default` | string |  |
| `servicePlan.settings.certifyOptions.selected[]` | string |  |
| `servicePlan.settings.emailOtp` | boolean |  |
| `servicePlan.settings.pdfCompliant` | boolean |  |
| `servicePlan.settings.readonlyUserFields` | object |  |
| `servicePlan.settings.signatureType` | string |  |
| `servicePlan.settings.signingKeysWithPassword` | boolean |  |
| `servicePlan.settings.smsNotification` | boolean |  |
| `servicePlan.settings.smsOtp` | boolean |  |
| `servicePlan.settings.smsOtpLength` | number |  |
| `servicePlan.settings.smsOtpRetryDuration` | number |  |
| `servicePlan.settings.totp` | boolean |  |
| `servicePlan.settings.workflowEvidence` | string |  |
| `servicePlan.signaturePad.enabled` | boolean |  |
| `servicePlan.signaturePad.server` | object |  |
| `servicePlan.signatureSettings.levelOfAssurance.selected[]` | string |  |
| `servicePlan.signatureSettings.signingServers[].capacity.advancedElectronicSeal.enabled` | boolean |  |
| `servicePlan.signatureSettings.signingServers[].capacity.advancedElectronicSignature.enabled` | boolean |  |
| `servicePlan.signatureSettings.signingServers[].capacity.advancedElectronicSignature.selected[].id` | number |  |
| `servicePlan.signatureSettings.signingServers[].capacity.advancedElectronicSignature.selected[].keyProtection` | string |  |
| `servicePlan.signatureSettings.signingServers[].capacity.advancedElectronicSignature.selected[].levelOfAssurance` | string |  |
| `servicePlan.signatureSettings.signingServers[].capacity.advancedElectronicSignature.selected[].name` | string |  |
| `servicePlan.signatureSettings.signingServers[].capacity.electronicSeal.enabled` | boolean |  |
| `servicePlan.signatureSettings.signingServers[].capacity.electronicSeal.selected[].id` | number |  |
| `servicePlan.signatureSettings.signingServers[].capacity.electronicSeal.selected[].keyProtection` | string |  |
| `servicePlan.signatureSettings.signingServers[].capacity.electronicSeal.selected[].levelOfAssurance` | string |  |
| `servicePlan.signatureSettings.signingServers[].capacity.electronicSeal.selected[].name` | string |  |
| `servicePlan.signatureSettings.signingServers[].capacity.highTrustAdvanced.enabled` | boolean |  |
| `servicePlan.signatureSettings.signingServers[].capacity.qualifiedElectronicSeal.enabled` | boolean |  |
| `servicePlan.signatureSettings.signingServers[].capacity.qualifiedElectronicSignature.enabled` | boolean |  |
| `servicePlan.signatureSettings.signingServers[].info.appearanceDesignName` | object |  |
| `servicePlan.signatureSettings.signingServers[].info.appearanceLogo` | object |  |
| `servicePlan.signatureSettings.signingServers[].info.authType` | object |  |
| `servicePlan.signatureSettings.signingServers[].info.id` | number |  |
| `servicePlan.signatureSettings.signingServers[].info.keyLocation` | string |  |
| `servicePlan.signatureSettings.signingServers[].info.levelOfAssurance` | object |  |
| `servicePlan.signatureSettings.signingServers[].info.name` | string |  |
| `servicePlan.signatureSettings.signingServers[].info.order` | object |  |
| `servicePlan.signatureSettings.signingServers[].info.provider` | string |  |
| `servicePlan.signatureSettings.signingServers[].info.signatureType[]` | string |  |
| `servicePlan.startDate` | string |  |
| `servicePlan.type` | string |  |
| `timeZone` | string |  |
| `twoFactorAuthenticationEnabled` | boolean |  |
| `userEmail` | string |  |
| `userId` | number |  |
| `userName` | string |  |
| `userNationalId` | object |  |

## Native endpoint

Through the native SigningHub API, this operation is `GET /v4/account` (base URL `https://api.signinghub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.

