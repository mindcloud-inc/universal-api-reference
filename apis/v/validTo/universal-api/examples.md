# validTo Universal API Examples

These examples use the MindCloud API key and validTo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Credit Balance

Retrieves your credit balance from validTo.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/validTo/latest/actions/get-credit-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/validTo/latest/actions/get-credit-balance?${params}`, {
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
      "creditsInfo": {},
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Get Credit Balance action reference](actions/get-credit-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/validTo/latest/actions/get-credit-balance).

## Create Bulk Validation List

Creates a bulk validation list in validTo.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/validTo/latest/actions/create-bulk-validation-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "local_file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/validTo/latest/actions/create-bulk-validation-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "local_file": "string"
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
      "job_id": "string",
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Create Bulk Validation List action reference](actions/create-bulk-validation-list.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/validTo/latest/actions/create-bulk-validation-list).
