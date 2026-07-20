# Peggy Pay Universal API Examples

These examples use the MindCloud API key and Peggy Pay connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Authorize API Key

Retrieves an access token from Peggy Pay.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/peggyPay/latest/actions/authorize-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/peggyPay/latest/actions/authorize-api-key?${params}`, {
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
      "Token": "string"
    }
  ],
  "meta": {}
}
```

See the full [Authorize API Key action reference](actions/authorize-api-key.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/peggyPay/latest/actions/authorize-api-key).

## Add Submission Item

Updates a Peggy Pay submission by adding an item.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/peggyPay/latest/actions/add-submission-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "hash": "abc123submissionhash",
  "itemKey": "externalReference",
  "itemLabel": "External reference",
  "itemValue": "ORD-1001"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/peggyPay/latest/actions/add-submission-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "hash": "abc123submissionhash",
    "itemKey": "externalReference",
    "itemLabel": "External reference",
    "itemValue": "ORD-1001"
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
      "data": {},
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Add Submission Item action reference](actions/add-submission-item.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/peggyPay/latest/actions/add-submission-item).
