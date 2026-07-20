# SE Ranking Data Universal API Examples

These examples use the MindCloud API key and SE Ranking Data connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Subscription Details

Retrieves subscription details from SE Ranking Data.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-subscription-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-subscription-details?${params}`, {
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
      "subscriptionInfo": {
        "expiratonDate": "string",
        "startDate": "string",
        "status": "string",
        "unitsLeft": "string",
        "unitsLimit": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Subscription Details action reference](actions/get-subscription-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/seRanking/latest/actions/get-subscription-details).

## Create advanced audit

Creates an advanced website audit in SE Ranking Data.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/create-advanced-audit" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "domain": "seranking.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/create-advanced-audit', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "domain": "seranking.com"
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
      "id": 1
    }
  ],
  "meta": {}
}
```

See the full [Create advanced audit action reference](actions/create-advanced-audit.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/seRanking/latest/actions/create-advanced-audit).
