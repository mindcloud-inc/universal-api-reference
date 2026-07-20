# SigningHub Universal API Examples

These examples use the MindCloud API key and SigningHub connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account

Retrieves account details from SigningHub.

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

Example response:

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

See the full [Get Account action reference](actions/get-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/signingHub/latest/actions/get-account).

## Add Digital Signature Field

Adds a digital signature field in SigningHub.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/add-digital-signature-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "packageId": "11191528",
  "documentId": "13459082",
  "order": "1",
  "pageNo": "1",
  "levelOfAssurance": "ELECTRONIC_SIGNATURE",
  "x": "40",
  "y": "100",
  "width": "150",
  "height": "40"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/add-digital-signature-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "packageId": "11191528",
    "documentId": "13459082",
    "order": "1",
    "pageNo": "1",
    "levelOfAssurance": "ELECTRONIC_SIGNATURE",
    "x": "40",
    "y": "100",
    "width": "150",
    "height": "40"
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
      "created_on": "2026-05-07T12:00:00.000Z",
      "field_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Add Digital Signature Field action reference](actions/add-digital-signature-field.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/signingHub/latest/actions/add-digital-signature-field).
