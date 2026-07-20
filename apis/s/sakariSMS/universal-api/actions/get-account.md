# Sakari SMS: Get Account

Retrieves an account from Sakari SMS.

```
GET https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sakari SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/get-account?${params}`, {
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
      "apiCredentials": {
        "id": "string",
        "secret": "string"
      },
      "balance": 1,
      "billing": {
        "address": {
          "city": "string",
          "country": {},
          "line1": "string",
          "line2": "string",
          "postalCode": "string",
          "state": "string"
        },
        "email": "ava@example.com",
        "name": "Ava Chen",
        "tax": {}
      },
      "defaults": {
        "country": {
          "code": "string",
          "name": "Ava Chen"
        }
      },
      "externalName": "Ava Chen",
      "id": "string",
      "info": {
        "address": {
          "city": "string",
          "country": {},
          "line1": "string",
          "line2": "string",
          "postalCode": "string",
          "state": "string"
        },
        "email": "ava@example.com",
        "phone": "string",
        "website": "string"
      },
      "integrations": {},
      "legalName": "Ava Chen",
      "name": "Ava Chen",
      "nextBillingDate": "string",
      "options": {
        "autoEnroll": {
          "domain": "string",
          "notifyEmail": "ava@example.com",
          "role": "string"
        },
        "autoLinkShorten": true,
        "autotopup": {
          "amount": 1,
          "below": 1,
          "lastTopup": "2026-05-07T12:00:00.000Z"
        },
        "customDomain": {
          "created": {},
          "domain": "string",
          "id": "string",
          "renewAt": "string",
          "verified": "string"
        },
        "universalMMS": true,
        "verifyNumberType": true
      },
      "partner": {
        "approved": "2026-05-07T12:00:00.000Z",
        "contact": "string",
        "paypalEmail": "ava@example.com",
        "rejected": "2026-05-07T12:00:00.000Z",
        "submitted": "2026-05-07T12:00:00.000Z"
      },
      "plan": {
        "billingFrequency": "string",
        "commitment": 1,
        "credit": 1,
        "id": "string",
        "includedPhoneNumberCountries": [
          "string"
        ],
        "maxCommitment": 1,
        "minCommitment": 1,
        "name": "Ava Chen",
        "passThroughPlanEligible": true,
        "price": 1,
        "pricing": {}
      },
      "promoCode": "string",
      "questionare": {},
      "questionnaire": {},
      "referralCode": "string",
      "referrer": "string",
      "subscription": {
        "activeUntil": "string"
      },
      "trialExpiry": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiCredentials` | object |  |
| `apiCredentials.id` | string |  |
| `apiCredentials.secret` | string |  |
| `balance` | number |  |
| `billing` | object |  |
| `billing.address` | object |  |
| `billing.address.city` | string |  |
| `billing.address.country` | object |  |
| `billing.address.line1` | string |  |
| `billing.address.line2` | string |  |
| `billing.address.postalCode` | string |  |
| `billing.address.state` | string |  |
| `billing.email` | string |  |
| `billing.name` | string |  |
| `billing.tax` | object |  |
| `defaults` | object |  |
| `defaults.country` | object |  |
| `defaults.country.code` | string |  |
| `defaults.country.name` | string |  |
| `externalName` | string |  |
| `id` | string |  |
| `info` | object |  |
| `info.address` | object |  |
| `info.address.city` | string |  |
| `info.address.country` | object |  |
| `info.address.line1` | string |  |
| `info.address.line2` | string |  |
| `info.address.postalCode` | string |  |
| `info.address.state` | string |  |
| `info.email` | string |  |
| `info.phone` | string |  |
| `info.website` | string |  |
| `integrations` | object |  |
| `legalName` | string |  |
| `name` | string |  |
| `nextBillingDate` | string |  |
| `options` | object |  |
| `options.autoEnroll` | object |  |
| `options.autoEnroll.domain` | string |  |
| `options.autoEnroll.notifyEmail` | string |  |
| `options.autoEnroll.role` | string |  |
| `options.autoLinkShorten` | boolean |  |
| `options.autotopup` | object |  |
| `options.autotopup.amount` | number |  |
| `options.autotopup.below` | number |  |
| `options.autotopup.lastTopup` | date |  |
| `options.customDomain` | object |  |
| `options.customDomain.created` | object |  |
| `options.customDomain.domain` | string |  |
| `options.customDomain.id` | string |  |
| `options.customDomain.renewAt` | string |  |
| `options.customDomain.verified` | string |  |
| `options.universalMMS` | boolean |  |
| `options.verifyNumberType` | boolean |  |
| `partner` | object |  |
| `partner.approved` | date |  |
| `partner.contact` | string |  |
| `partner.paypalEmail` | string |  |
| `partner.rejected` | date |  |
| `partner.submitted` | date |  |
| `plan` | object |  |
| `plan.billingFrequency` | string |  |
| `plan.commitment` | number |  |
| `plan.credit` | number |  |
| `plan.id` | string |  |
| `plan.includedPhoneNumberCountries` | array<string> |  |
| `plan.maxCommitment` | number |  |
| `plan.minCommitment` | number |  |
| `plan.name` | string |  |
| `plan.passThroughPlanEligible` | boolean |  |
| `plan.price` | number |  |
| `plan.pricing` | object |  |
| `promoCode` | string |  |
| `questionare` | object |  |
| `questionnaire` | object |  |
| `referralCode` | string |  |
| `referrer` | string |  |
| `subscription` | object |  |
| `subscription.activeUntil` | string |  |
| `trialExpiry` | date |  |

## Native endpoint

Through the native Sakari SMS API, this operation is `GET /v1/accounts/:accountId` (base URL `https://api.sakari.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.

