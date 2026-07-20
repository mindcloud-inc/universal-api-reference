# jo4.io Universal API Examples

These examples use the MindCloud API key and jo4.io connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List API Keys



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/list-api-keys?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/list-api-keys?${params}`, {
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
      "createdTime": 1,
      "description": "string",
      "enabled": true,
      "expired": true,
      "expiresAt": 1,
      "id": 1,
      "keyPrefix": "string",
      "lastUsedAt": 1,
      "lastUsedIp": "string",
      "modifiedTime": 1,
      "name": "Ava Chen",
      "scopes": [
        "string"
      ],
      "slug": "string",
      "useCount": 1
    }
  ],
  "meta": {}
}
```

See the full [List API Keys action reference](actions/list-api-keys.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/jo4io/latest/actions/list-api-keys).

## Add Domain



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/add-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "domain": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/add-domain', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "domain": "string"
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
      "cnameTarget": "Ava Chen",
      "createdTime": 1,
      "dnsTxtRecordName": "Ava Chen",
      "dnsTxtRecordValue": "string",
      "domain": "string",
      "hostnameStatus": "Ava Chen",
      "id": 1,
      "modifiedTime": 1,
      "ready": true,
      "slug": "string",
      "sslProvisionedAt": 1,
      "sslStatus": "string",
      "sslTxtName": "Ava Chen",
      "sslTxtValue": "string",
      "userId": 1,
      "verified": true,
      "verifiedAt": 1
    }
  ],
  "meta": {}
}
```

See the full [Add Domain action reference](actions/add-domain.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/jo4io/latest/actions/add-domain).
