# Amazing Marvin Universal API Examples

These examples use the MindCloud API key and Amazing Marvin connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Test Credentials

Tests API credentials in Amazing Marvin.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amazingMarvin/latest/actions/test-credentials?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amazingMarvin/latest/actions/test-credentials?${params}`, {
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
      "response": "string"
    }
  ],
  "meta": {}
}
```

See the full [Test Credentials action reference](actions/test-credentials.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/amazingMarvin/latest/actions/test-credentials).

## Claim Reward Points

Claims reward points in Amazing Marvin.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/amazingMarvin/latest/actions/claim-reward-points" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "points": 1,
  "itemId": "MANUAL",
  "date": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/amazingMarvin/latest/actions/claim-reward-points', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "points": 1,
    "itemId": "MANUAL",
    "date": "string"
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
      "billingPeriod": "string",
      "currentVersion": "string",
      "defaultAutoSnooze": true,
      "defaultOffset": 1,
      "defaultSnooze": 1,
      "email": "ava@example.com",
      "emailConfirmed": true,
      "iosSub": true,
      "marvinPoints": 1,
      "nextMultiplier": 1,
      "paidThrough": "2026-05-07T12:00:00.000Z",
      "parentEmail": "ava@example.com",
      "rewardPointsEarned": 1,
      "rewardPointsEarnedToday": 1,
      "rewardPointsLastDate": "2026-05-07T12:00:00.000Z",
      "rewardPointsSpent": 1,
      "rewardPointsSpentToday": 1,
      "signupAppVersion": "string",
      "tomatoDate": "string",
      "tomatoes": 1,
      "tomatoesToday": 1,
      "tomatoTime": 1,
      "tomatoTimeToday": 1,
      "tracking": "string",
      "trackingSince": 1,
      "userId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Claim Reward Points action reference](actions/claim-reward-points.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/amazingMarvin/latest/actions/claim-reward-points).
