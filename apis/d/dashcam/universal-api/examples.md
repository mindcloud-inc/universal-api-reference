# Dashcam Universal API Examples

These examples use the MindCloud API key and Dashcam connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Billing Usage

Retrieves billing usage from Dashcam.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dashcam/latest/actions/get-billing-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dashcam/latest/actions/get-billing-usage?${params}`, {
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
      "accountStartDate": 1,
      "daily": {},
      "includedMinutes": 1,
      "includedSeconds": 1,
      "isTrialUser": true,
      "monthly": {},
      "plan": "string",
      "pricing": {},
      "remainingMinutes": 1,
      "remainingSeconds": 1,
      "totalUsedMinutes": 1,
      "totalUsedSeconds": 1,
      "unlimited": true,
      "usagePercentage": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Billing Usage action reference](actions/get-billing-usage.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dashcam/latest/actions/get-billing-usage).

## Clone Replay

Clones a replay in Dashcam.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dashcam/latest/actions/clone-replay" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dashcam/latest/actions/clone-replay', {
  method: 'PUT',
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
  "data": [],
  "meta": {}
}
```

See the full [Clone Replay action reference](actions/clone-replay.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dashcam/latest/actions/clone-replay).
