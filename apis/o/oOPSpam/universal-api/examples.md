# OOPSpam Universal API Examples

These examples use the MindCloud API key and OOPSpam connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check Domain Reputation

Checks a domain's reputation in OOPSpam.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oOPSpam/latest/actions/check-domain-reputation?connectionId=$CONNECTION_ID&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oOPSpam/latest/actions/check-domain-reputation?${params}`, {
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
      "blocked": true,
      "blocker": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Check Domain Reputation action reference](actions/check-domain-reputation.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/oOPSpam/latest/actions/check-domain-reputation).

## Check Content for Spam

Checks submitted content for spam in OOPSpam.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oOPSpam/latest/actions/check-content-for-spam" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oOPSpam/latest/actions/check-content-for-spam', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "details": {
        "isEmailBlocked": true,
        "numberOfSpamWords": 1
      },
      "score": 1
    }
  ],
  "meta": {}
}
```

See the full [Check Content for Spam action reference](actions/check-content-for-spam.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/oOPSpam/latest/actions/check-content-for-spam).
