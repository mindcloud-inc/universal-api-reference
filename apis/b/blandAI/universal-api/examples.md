# Bland AI Universal API Examples

These examples use the MindCloud API key and Bland AI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Account Details

Retrieves account details from your Bland AI account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blandAI/latest/actions/account-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blandAI/latest/actions/account-details?${params}`, {
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
      "billing": {
        "currentBalance": 1,
        "refillTo": "string"
      },
      "status": "string",
      "totalCalls": 1
    }
  ],
  "meta": {}
}
```

See the full [Account Details action reference](actions/account-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/blandAI/latest/actions/account-details).

## Create Batch

Creates a new call batch in Bland AI.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/blandAI/latest/actions/create-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "global": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blandAI/latest/actions/create-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "global": {}
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
      "data": {}
    }
  ],
  "meta": {}
}
```

See the full [Create Batch action reference](actions/create-batch.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/blandAI/latest/actions/create-batch).
