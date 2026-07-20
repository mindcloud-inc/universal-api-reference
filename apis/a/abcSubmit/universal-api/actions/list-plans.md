# AbcSubmit: List Plans

Retrieves public subscription plans from AbcSubmit.

```
GET https://connect.mindcloud.co/v1/universal/abcSubmit/latest/actions/list-plans
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AbcSubmit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/abcSubmit/latest/actions/list-plans?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/abcSubmit/latest/actions/list-plans?${params}`, {
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
        "maxNumberOfFields": {},
        "maxNumberOfRules": {},
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
        ]
      },
      "planIdMonthly": "string",
      "planIdYearly": "string",
      "priceMonthlyCents": 1,
      "priceYearlyCents": 1,
      "whiteLabelDomain": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `branding` | boolean |  |
| `customFeaturesAndPricing` | boolean |  |
| `encryptedSubmissions` | boolean |  |
| `featuredPlan` | boolean |  |
| `id` | number |  |
| `isPublic` | boolean |  |
| `maxFormsCount` | number |  |
| `maxMailsSentDaily` | number |  |
| `maxStorageNumFiles` | number |  |
| `maxStorageQuota` | number |  |
| `maxSubmissionsCount` | number |  |
| `maxSubuserAccounts` | number |  |
| `name` | string |  |
| `nextUpgradePlanId` | number |  |
| `planFeatures.maxNumberOfFields` | object |  |
| `planFeatures.maxNumberOfRules` | object |  |
| `planFeatures.supportsBigDataCollections` | boolean |  |
| `planFeatures.supportsCustomSmtp` | number |  |
| `planFeatures.supportsIntegrations` | boolean |  |
| `planFeatures.supportsNewsletters` | boolean |  |
| `planFeatures.supportsPayments` | boolean |  |
| `planFeatures.supportsSaveForLater` | boolean |  |
| `planFeatures.supportsStorage` | boolean |  |
| `planFeatures.supportsTranslations` | boolean |  |
| `planFeatures.supportsWorkflows` | boolean |  |
| `planFeatures.unsupportedControls[]` | number |  |
| `planFeatures.unsupportedIntegrations[]` | number |  |
| `planIdMonthly` | string |  |
| `planIdYearly` | string |  |
| `priceMonthlyCents` | number |  |
| `priceYearlyCents` | number |  |
| `whiteLabelDomain` | boolean |  |

## Native endpoint

Through the native AbcSubmit API, this operation is `GET /api/v1/users/plans` (base URL `https://www.abcsubmit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-plans.md) for the provider-specific parameters and requirements.

