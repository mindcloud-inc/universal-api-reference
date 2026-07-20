# Dwolla Universal API Examples

These examples use the MindCloud API key and Dwolla connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Root

Retrieves the API root for accessible Dwolla resources.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/get-root?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/get-root?${params}`, {
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
      "_links": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Root action reference](actions/get-root.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dwolla/latest/actions/get-root).

## Cancel Transfer

Cancels a pending transfer in Dwolla.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/cancel-transfer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/cancel-transfer', {
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
  "data": [
    {
      "_links": {},
      "amount": {},
      "created": "string",
      "id": "string",
      "individualAchId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Cancel Transfer action reference](actions/cancel-transfer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dwolla/latest/actions/cancel-transfer).
