# AbcSubmit Universal API Examples

These examples use the MindCloud API key and AbcSubmit connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get My Plan

Retrieves your current AbcSubmit plan limits.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/abcSubmit/latest/actions/get-my-plan?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/abcSubmit/latest/actions/get-my-plan?${params}`, {
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
      "branding": true,
      "customFeaturesAndPricing": true,
      "encryptedSubmissions": true,
      "featuredPlan": true,
      "id": 1,
      "isPublic": true,
      "maxFormsCount": 1,
      "maxMailsSentDaily": 1,
      "maxStorageNumFiles": 1,
      "maxStorageQuota": 1,
      "maxSubmissionsCount": 1,
      "maxSubuserAccounts": 1,
      "name": "Ava Chen",
      "nextUpgradePlanId": 1,
      "planFeatures": {
        "maxNumberOfFields": 1,
        "maxNumberOfRules": 1,
        "supportsBigDataCollections": true,
        "supportsCustomSmtp": 1,
        "supportsIntegrations": true,
        "supportsNewsletters": true,
        "supportsPayments": true,
        "supportsSaveForLater": true,
        "supportsStorage": true,
        "supportsTranslations": true,
        "supportsWorkflows": true,
        "unsupportedControls": [
          1
        ],
        "unsupportedIntegrations": [
          1
        ],
        "unsupportedPaymentGateways": [
          1
        ]
      },
      "priceMonthlyCents": 1,
      "priceYearlyCents": 1,
      "whiteLabelDomain": true
    }
  ],
  "meta": {}
}
```

See the full [Get My Plan action reference](actions/get-my-plan.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/abcSubmit/latest/actions/get-my-plan).

## Change Password

Updates a user's password in AbcSubmit.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/abcSubmit/latest/actions/change-password" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "oldPassword": "string",
  "newPassword": "string",
  "confirmPassword": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/abcSubmit/latest/actions/change-password', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "oldPassword": "string",
    "newPassword": "string",
    "confirmPassword": "string"
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
      "response": true
    }
  ],
  "meta": {}
}
```

See the full [Change Password action reference](actions/change-password.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/abcSubmit/latest/actions/change-password).
