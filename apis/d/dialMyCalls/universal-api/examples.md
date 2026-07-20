# DialMyCalls Universal API Examples

These examples use the MindCloud API key and DialMyCalls connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account

Retrieves your account details from DialMyCalls.

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

Example response:

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

See the full [Get Account action reference](actions/get-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dialMyCalls/latest/actions/get-account).

## Add Caller ID

Creates a new caller ID in DialMyCalls.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dialMyCalls/latest/actions/add-caller-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "phone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dialMyCalls/latest/actions/add-caller-id', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "phone": "string"
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
      "approved": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "phone": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Add Caller ID action reference](actions/add-caller-id.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dialMyCalls/latest/actions/add-caller-id).
