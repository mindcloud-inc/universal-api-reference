# EmailListVerify Universal API Examples

These examples use the MindCloud API key and EmailListVerify connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Credits

Retrieves your available credits from EmailListVerify.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emailListVerify/latest/actions/get-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emailListVerify/latest/actions/get-credits?${params}`, {
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
      "onDemand": {
        "available": 1
      },
      "subscription": {
        "available": 1,
        "expiresAt": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Credits action reference](actions/get-credits.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/emailListVerify/latest/actions/get-credits).

## Create Email Verification Job

Creates an asynchronous email verification job in EmailListVerify.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/emailListVerify/latest/actions/create-email-verification-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/emailListVerify/latest/actions/create-email-verification-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com"
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
      "email": "ava@example.com",
      "id": "string",
      "quality": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Email Verification Job action reference](actions/create-email-verification-job.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/emailListVerify/latest/actions/create-email-verification-job).
