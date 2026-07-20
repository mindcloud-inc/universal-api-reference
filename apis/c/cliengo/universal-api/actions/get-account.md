# Cliengo: Get Account



```
GET https://connect.mindcloud.co/v1/universal/cliengo/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cliengo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cliengo/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cliengo/latest/actions/get-account?${params}`, {
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
      "chatUrl": "https://example.com",
      "contactName": "Ava Chen",
      "countryId": "string",
      "creationDate": "string",
      "email": "ava@example.com",
      "freeTrialExpirationDate": "string",
      "hasConversationPlan": true,
      "hasSubscription": true,
      "id": "string",
      "labs": {},
      "language": "string",
      "leadCount": 1,
      "leadCountTotal": 1,
      "leadLimit": 1,
      "marketingCampaignsInfo": {},
      "name": "Ava Chen",
      "phone": "string",
      "planCurrency": "string",
      "planFrequency": "string",
      "planLimits": [
        {}
      ],
      "planName": "Ava Chen",
      "planPrice": 1,
      "planShortName": "Ava Chen",
      "planType": "string",
      "quickstartSteps": {},
      "tags": {},
      "timeZone": "string",
      "userCount": 1,
      "whiteLabelEmail": "ava@example.com",
      "whiteLabelId": "string",
      "whiteLabelLogoUrl": "https://example.com",
      "whiteLabelName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chatUrl` | string | Chat websocket URL. |
| `contactName` | string | Primary contact name. |
| `countryId` | string | Country code. |
| `creationDate` | string | Account creation timestamp returned by Cliengo. |
| `email` | string | Primary account email. |
| `freeTrialExpirationDate` | string | Free trial expiration timestamp. |
| `hasConversationPlan` | boolean | Whether the account has a conversation plan. |
| `hasSubscription` | boolean | Whether the account has an active subscription. |
| `id` | string | Cliengo account identifier. |
| `labs` | object | Feature-flag and lab settings. |
| `language` | string | Account language. |
| `leadCount` | number | Current lead count. |
| `leadCountTotal` | number | Total lead count. |
| `leadLimit` | number | Lead limit for the current plan. |
| `marketingCampaignsInfo` | object | Marketing campaign metadata. |
| `name` | string | Account display name. |
| `phone` | string | Primary account phone number. |
| `planCurrency` | string | Plan billing currency. |
| `planFrequency` | string | Plan billing frequency. |
| `planLimits` | array<object> | Per-unit plan limits. |
| `planName` | string | Plan display name. |
| `planPrice` | number | Plan price. |
| `planShortName` | string | Short plan description. |
| `planType` | string | Plan type code. |
| `quickstartSteps` | object | Quickstart completion flags. |
| `tags` | object | Tag metadata object. |
| `timeZone` | string | Configured time zone. |
| `userCount` | number | Current user count. |
| `whiteLabelEmail` | string | White label contact email. |
| `whiteLabelId` | string | White label identifier. |
| `whiteLabelLogoUrl` | string | White label logo URL. |
| `whiteLabelName` | string | White label display name. |

## Native endpoint

Through the native Cliengo API, this operation is `GET /account` (base URL `https://api.cliengo.com/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.

