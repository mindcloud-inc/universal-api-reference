# One-Time Secret Universal API Examples

These examples use the MindCloud API key and One-Time Secret connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Receipts

Retrieves recent secret receipts from One-Time Secret.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneTimeSecret/latest/actions/v2-list-receipts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneTimeSecret/latest/actions/v2-list-receipts?${params}`, {
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
      "count": 1,
      "details": {},
      "records": [
        {}
      ],
      "shrimp": "string",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Receipts action reference](actions/v2-list-receipts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/oneTimeSecret/latest/actions/v2-list-receipts).

## Conceal Secret

Creates a new secret from provided content in One-Time Secret.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oneTimeSecret/latest/actions/v2-conceal-secret" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "secret.shareDomain": "us.onetimesecret.com",
  "secret.secret": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneTimeSecret/latest/actions/v2-conceal-secret', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "secret.shareDomain": "us.onetimesecret.com",
    "secret.secret": "string"
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
      "details": {},
      "record": {},
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Conceal Secret action reference](actions/v2-conceal-secret.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/oneTimeSecret/latest/actions/v2-conceal-secret).
