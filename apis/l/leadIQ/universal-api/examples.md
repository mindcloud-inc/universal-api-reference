# LeadIQ Universal API Examples

These examples use the MindCloud API key and LeadIQ connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadIQ/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadIQ/latest/actions/get-account?${params}`, {
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
      "dataHubPlan": {
        "available": 1,
        "name": "Ava Chen",
        "nextBillingPeriod": "2026-05-07T12:00:00.000Z",
        "product": "string",
        "status": "string",
        "used": 1
      },
      "plans": [
        {
          "name": "Ava Chen",
          "nextBillingPeriod": "2026-05-07T12:00:00.000Z",
          "product": "string",
          "status": "string"
        }
      ],
      "universalPlan": {
        "available": 1,
        "name": "Ava Chen",
        "nextBillingPeriod": "2026-05-07T12:00:00.000Z",
        "product": "string",
        "status": "string",
        "used": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Account action reference](actions/get-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/leadIQ/latest/actions/get-account).

## Submit Person Feedback



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/leadIQ/latest/actions/submit-person-feedback" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leadIQ/latest/actions/submit-person-feedback', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "value": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Submit Person Feedback action reference](actions/submit-person-feedback.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/leadIQ/latest/actions/submit-person-feedback).
