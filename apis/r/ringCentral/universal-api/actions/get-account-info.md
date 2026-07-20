# RingCentral: Get Account Info

Retrieves the current RingCentral account information.

```
GET https://connect.mindcloud.co/v1/universal/ringCentral/latest/actions/get-account-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RingCentral `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ringCentral/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ringCentral/latest/actions/get-account-info?${params}`, {
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
      "bsid": "string",
      "federated": true,
      "id": "string",
      "limits": {
        "cloudRecordingStorage": 1,
        "freeSoftPhoneLinesPerExtension": 1,
        "maxExtensionNumberLength": 1,
        "maxMonitoredExtensionsPerUser": 1,
        "meetingSize": 1
      },
      "mainNumber": "string",
      "operator": {
        "extensionNumber": "string",
        "id": "string",
        "uri": "string"
      },
      "regionalSettings": {
        "currency": {
          "code": "string",
          "id": "string",
          "minorSymbol": "string",
          "name": "Ava Chen",
          "symbol": "string"
        },
        "formattingLocale": {
          "id": "string",
          "localeCode": "string",
          "name": "Ava Chen"
        },
        "greetingLanguage": {
          "id": "string",
          "localeCode": "string",
          "name": "Ava Chen"
        },
        "homeCountry": {
          "id": "string",
          "name": "Ava Chen",
          "uri": "string"
        },
        "language": {
          "id": "string",
          "localeCode": "string",
          "name": "Ava Chen"
        },
        "timeFormat": "string",
        "timezone": {
          "bias": "string",
          "description": "string",
          "id": "string",
          "name": "Ava Chen",
          "uri": "string"
        }
      },
      "serviceInfo": {
        "billingPlan": {
          "duration": 1,
          "durationUnit": "string",
          "id": "string",
          "includedPhoneLines": 1,
          "name": "Ava Chen",
          "type": "string"
        },
        "brand": {
          "homeCountry": {
            "callingCode": "string",
            "id": "string",
            "isoCode": "string",
            "name": "Ava Chen",
            "uri": "string"
          },
          "id": "string",
          "name": "Ava Chen"
        },
        "contractedCountry": {
          "id": "string",
          "isoCode": "string",
          "name": "Ava Chen",
          "uri": "string"
        },
        "servicePlan": {
          "edition": "string",
          "id": "string",
          "name": "Ava Chen"
        },
        "uri": "string"
      },
      "setupWizardState": "string",
      "signupInfo": {
        "creationTime": "string",
        "marketingAccepted": true,
        "tosAccepted": true
      },
      "status": "string",
      "uri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bsid` | string |  |
| `federated` | boolean |  |
| `id` | string |  |
| `limits.cloudRecordingStorage` | number |  |
| `limits.freeSoftPhoneLinesPerExtension` | number |  |
| `limits.maxExtensionNumberLength` | number |  |
| `limits.maxMonitoredExtensionsPerUser` | number |  |
| `limits.meetingSize` | number |  |
| `mainNumber` | string |  |
| `operator.extensionNumber` | string |  |
| `operator.id` | string |  |
| `operator.uri` | string |  |
| `regionalSettings.currency.code` | string |  |
| `regionalSettings.currency.id` | string |  |
| `regionalSettings.currency.minorSymbol` | string |  |
| `regionalSettings.currency.name` | string |  |
| `regionalSettings.currency.symbol` | string |  |
| `regionalSettings.formattingLocale.id` | string |  |
| `regionalSettings.formattingLocale.localeCode` | string |  |
| `regionalSettings.formattingLocale.name` | string |  |
| `regionalSettings.greetingLanguage.id` | string |  |
| `regionalSettings.greetingLanguage.localeCode` | string |  |
| `regionalSettings.greetingLanguage.name` | string |  |
| `regionalSettings.homeCountry.id` | string |  |
| `regionalSettings.homeCountry.name` | string |  |
| `regionalSettings.homeCountry.uri` | string |  |
| `regionalSettings.language.id` | string |  |
| `regionalSettings.language.localeCode` | string |  |
| `regionalSettings.language.name` | string |  |
| `regionalSettings.timeFormat` | string |  |
| `regionalSettings.timezone.bias` | string |  |
| `regionalSettings.timezone.description` | string |  |
| `regionalSettings.timezone.id` | string |  |
| `regionalSettings.timezone.name` | string |  |
| `regionalSettings.timezone.uri` | string |  |
| `serviceInfo.billingPlan.duration` | number |  |
| `serviceInfo.billingPlan.durationUnit` | string |  |
| `serviceInfo.billingPlan.id` | string |  |
| `serviceInfo.billingPlan.includedPhoneLines` | number |  |
| `serviceInfo.billingPlan.name` | string |  |
| `serviceInfo.billingPlan.type` | string |  |
| `serviceInfo.brand.homeCountry.callingCode` | string |  |
| `serviceInfo.brand.homeCountry.id` | string |  |
| `serviceInfo.brand.homeCountry.isoCode` | string |  |
| `serviceInfo.brand.homeCountry.name` | string |  |
| `serviceInfo.brand.homeCountry.uri` | string |  |
| `serviceInfo.brand.id` | string |  |
| `serviceInfo.brand.name` | string |  |
| `serviceInfo.contractedCountry.id` | string |  |
| `serviceInfo.contractedCountry.isoCode` | string |  |
| `serviceInfo.contractedCountry.name` | string |  |
| `serviceInfo.contractedCountry.uri` | string |  |
| `serviceInfo.servicePlan.edition` | string |  |
| `serviceInfo.servicePlan.id` | string |  |
| `serviceInfo.servicePlan.name` | string |  |
| `serviceInfo.uri` | string |  |
| `setupWizardState` | string |  |
| `signupInfo.creationTime` | string |  |
| `signupInfo.marketingAccepted` | boolean |  |
| `signupInfo.tosAccepted` | boolean |  |
| `status` | string |  |
| `uri` | string |  |

## Native endpoint

Through the native RingCentral API, this operation is `GET restapi/v1.0/account/~` (base URL `https://platform.ringcentral.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-info.md) for the provider-specific parameters and requirements.

