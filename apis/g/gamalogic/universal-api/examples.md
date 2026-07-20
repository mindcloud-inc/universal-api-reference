# Gamalogic Universal API Examples

These examples use the MindCloud API key and Gamalogic connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Credit Balance



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gamalogic/latest/actions/get-credit-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gamalogic/latest/actions/get-credit-balance?${params}`, {
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
      "creditBalance": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Credit Balance action reference](actions/get-credit-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gamalogic/latest/actions/get-credit-balance).

## Verify Batch Emails



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gamalogic/latest/actions/verify-batch-emails" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "gamalogicEmailidVrfy[]": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gamalogic/latest/actions/verify-batch-emails', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "gamalogicEmailidVrfy[]": "[object Object]"
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
      "batchId": 1,
      "error": true,
      "message": "string",
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

See the full [Verify Batch Emails action reference](actions/verify-batch-emails.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gamalogic/latest/actions/verify-batch-emails).
