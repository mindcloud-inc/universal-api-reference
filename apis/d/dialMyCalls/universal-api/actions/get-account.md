# DialMyCalls: Get Account

Retrieves your account details from DialMyCalls.

```
GET https://connect.mindcloud.co/v1/universal/dialMyCalls/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DialMyCalls `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dialMyCalls/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dialMyCalls/latest/actions/get-account?${params}`, {
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
      "account": {},
      "activeOauth": [
        "string"
      ],
      "alerts": [
        {}
      ],
      "callsPerMinute": 1,
      "callVariablesCredits": 1,
      "callVariablesPrice": 1,
      "capabilities": {},
      "contactsVersion": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creditsAvailable": 1,
      "currentUserId": 1,
      "currentUserName": "Ava Chen",
      "hasRecurringError": true,
      "id": 1,
      "inboundtexting": true,
      "inboundtextingVersion": "string",
      "intercomSettings": {},
      "maxMmsChars": 1,
      "maxMmsCredits": 1,
      "maxMmsLength": "string",
      "maxSmsChars": 1,
      "maxSmsCredits": 1,
      "maxSmsLength": "string",
      "messageLimit": 1,
      "mmsPrice": 1,
      "monthlyAllowsOverage": true,
      "name": "Ava Chen",
      "needsPhoneVerification": true,
      "needsTermsofservice": true,
      "onboardingCompletedSteps": [
        1
      ],
      "perms": {},
      "pft": {},
      "pttBalance": 1,
      "pusher": {},
      "referralUrl": "https://example.com",
      "smsPrefix": "string",
      "smsSuffix": "string",
      "statistics": {},
      "submemberid": 1,
      "upgrade": true,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | object |  |
| `activeOauth` | array<string> |  |
| `alerts` | array<object> |  |
| `callsPerMinute` | number |  |
| `callVariablesCredits` | number |  |
| `callVariablesPrice` | number |  |
| `capabilities` | object |  |
| `contactsVersion` | string |  |
| `createdAt` | date |  |
| `creditsAvailable` | number |  |
| `currentUserId` | number |  |
| `currentUserName` | string |  |
| `hasRecurringError` | boolean |  |
| `id` | number |  |
| `inboundtexting` | boolean |  |
| `inboundtextingVersion` | string |  |
| `intercomSettings` | object |  |
| `maxMmsChars` | number |  |
| `maxMmsCredits` | number |  |
| `maxMmsLength` | string |  |
| `maxSmsChars` | number |  |
| `maxSmsCredits` | number |  |
| `maxSmsLength` | string |  |
| `messageLimit` | number |  |
| `mmsPrice` | number |  |
| `monthlyAllowsOverage` | boolean |  |
| `name` | string |  |
| `needsPhoneVerification` | boolean |  |
| `needsTermsofservice` | boolean |  |
| `onboardingCompletedSteps` | array<number> |  |
| `perms` | object |  |
| `pft` | object |  |
| `pttBalance` | number |  |
| `pusher` | object |  |
| `referralUrl` | string |  |
| `smsPrefix` | string |  |
| `smsSuffix` | string |  |
| `statistics` | object |  |
| `submemberid` | number |  |
| `upgrade` | boolean |  |
| `uuid` | string |  |

## Native endpoint

Through the native DialMyCalls API, this operation is `GET /account` (base URL `https://{{credentials.apiKey}}@api.dialmycalls.com/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.

