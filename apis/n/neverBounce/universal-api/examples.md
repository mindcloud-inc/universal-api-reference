# NeverBounce Universal API Examples

These examples use the MindCloud API key and NeverBounce connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Info

Retrieves account details and usage information from NeverBounce.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neverBounce/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neverBounce/latest/actions/get-account-info?${params}`, {
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
      "creditsInfo": {
        "freeCreditsRemaining": 1,
        "freeCreditsUsed": 1,
        "paidCreditsRemaining": 1,
        "paidCreditsUsed": 1
      },
      "executionTime": 1,
      "jobCounts": {
        "completed": 1,
        "processing": 1,
        "queued": 1,
        "underReview": 1
      },
      "status": "string",
      "subscriptionType": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Account Info action reference](actions/get-account-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/neverBounce/latest/actions/get-account-info).

## Create Job From Remote URL

Creates a verification job in NeverBounce from a remote CSV URL.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/neverBounce/latest/actions/create-job-from-remote-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "remoteUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/neverBounce/latest/actions/create-job-from-remote-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "remoteUrl": "https://example.com"
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
      "executionTime": 1,
      "jobId": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Job From Remote URL action reference](actions/create-job-from-remote-url.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/neverBounce/latest/actions/create-job-from-remote-url).
