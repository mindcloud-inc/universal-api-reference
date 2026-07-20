# SPS Commerce Universal API Examples

These examples use the MindCloud API key and SPS Commerce connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Transaction

Retrieve a specific file.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sPSCommerce/latest/actions/get-transaction?connectionId=$CONNECTION_ID&filePath=testout%2FfileName.dat" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "filePath": "testout/fileName.dat"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sPSCommerce/latest/actions/get-transaction?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Get Transaction action reference](actions/get-transaction.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sPSCommerce/latest/actions/get-transaction).

## Create Transaction

This API accepts a payload that initiates a new transaction.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sPSCommerce/latest/actions/create-transaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "filePath": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sPSCommerce/latest/actions/create-transaction', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "filePath": "string"
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
      "path": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Transaction action reference](actions/create-transaction.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sPSCommerce/latest/actions/create-transaction).
