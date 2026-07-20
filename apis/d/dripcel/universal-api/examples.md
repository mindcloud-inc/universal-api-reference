# Dripcel Universal API Examples

These examples use the MindCloud API key and Dripcel connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Credit Balance

Retrieves the credit balance from Dripcel.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dripcel/latest/actions/get-credit-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dripcel/latest/actions/get-credit-balance?${params}`, {
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
      "data": 1,
      "ok": true,
      "requestId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Credit Balance action reference](actions/get-credit-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dripcel/latest/actions/get-credit-balance).

## Add Tags to Contact

Updates a contact to add tags in Dripcel.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dripcel/latest/actions/add-tags-to-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cell": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dripcel/latest/actions/add-tags-to-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cell": "string"
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
      "data": {
        "acknowledged": true,
        "matchedCount": 1,
        "modifiedCount": 1,
        "upsertedCount": 1,
        "upsertedId": {}
      },
      "ok": true,
      "requestId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Tags to Contact action reference](actions/add-tags-to-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dripcel/latest/actions/add-tags-to-contact).
