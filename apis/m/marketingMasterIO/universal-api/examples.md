# Marketing Master IO Universal API Examples

These examples use the MindCloud API key and Marketing Master IO connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Validate Access Token

Validates an access token in Marketing Master IO.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/validate-access-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/validate-access-token?${params}`, {
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
      "notice": "string",
      "status": true
    }
  ],
  "meta": {}
}
```

See the full [Validate Access Token action reference](actions/validate-access-token.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/marketingMasterIO/latest/actions/validate-access-token).

## Add Subscriber Tag

Adds a tag to a Messenger subscriber in Marketing Master IO.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/add-subscriber-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subscriber_id": "string",
  "tag": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/add-subscriber-tag', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subscriber_id": "string",
    "tag": "string"
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
      "status": true
    }
  ],
  "meta": {}
}
```

See the full [Add Subscriber Tag action reference](actions/add-subscriber-tag.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/marketingMasterIO/latest/actions/add-subscriber-tag).
