# Easymailing Universal API Examples

These examples use the MindCloud API key and Easymailing connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get My Subscription

Retrieves your subscription from Easymailing.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easymailing/latest/actions/get-my-subscription?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easymailing/latest/actions/get-my-subscription?${params}`, {
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
      "aiCostLimitCents": 1,
      "aiCostUsedCents": 1,
      "aiOverageLimitCents": {},
      "allowAiOverage": true,
      "audiences": 1,
      "automations": 1,
      "automationTriggers": 1,
      "canHaveAiOverage": true,
      "credits": 1,
      "creditsUsed": 1,
      "domain": "string",
      "expirationDate": "2026-05-07T12:00:00.000Z",
      "locale": "string",
      "maxSubscribers": 1,
      "subscribersUsed": 1,
      "tier": "string",
      "user": {
        "email": "ava@example.com",
        "firstname": "Ava",
        "lastname": {},
        "role": "string",
        "timezone": "string"
      },
      "websites": 1
    }
  ],
  "meta": {}
}
```

See the full [Get My Subscription action reference](actions/get-my-subscription.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/easymailing/latest/actions/get-my-subscription).
