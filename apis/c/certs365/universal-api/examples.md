# Certs 365 Universal API Examples

These examples use the MindCloud API key and Certs 365 connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Issuers

Retrieves issuer details from Certs 365.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/certs365/latest/actions/list-issuers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/certs365/latest/actions/list-issuers?${params}`, {
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
      "activeIssuers": 1,
      "allIssuers": 1,
      "code": 1,
      "data": [
        {}
      ],
      "inactiveIssuers": 1,
      "message": "string",
      "pendingIssuers": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Issuers action reference](actions/list-issuers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/certs365/latest/actions/list-issuers).

## Add Trusted Owner

Adds a trusted owner role in Certs 365.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/certs365/latest/actions/add-trusted-owner" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "address": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/certs365/latest/actions/add-trusted-owner', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "address": "string"
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
      "details": "string",
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Trusted Owner action reference](actions/add-trusted-owner.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/certs365/latest/actions/add-trusted-owner).
