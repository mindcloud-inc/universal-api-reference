# Emailable Universal API Examples

These examples use the MindCloud API key and Emailable connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Info

Retrieves account information from Emailable.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emailable/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emailable/latest/actions/get-account-info?${params}`, {
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
      "availableCredits": 1,
      "ownerEmail": "ava@example.com"
    }
  ],
  "meta": {}
}
```

See the full [Get Account Info action reference](actions/get-account-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/emailable/latest/actions/get-account-info).

## Create Verification Batch

Creates an email verification batch in Emailable.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/emailable/latest/actions/create-verification-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emails": "alice@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/emailable/latest/actions/create-verification-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emails": "alice@example.com"
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
      "id": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Verification Batch action reference](actions/create-verification-batch.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/emailable/latest/actions/create-verification-batch).
