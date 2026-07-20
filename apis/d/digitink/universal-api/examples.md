# Digit.ink Universal API Examples

These examples use the MindCloud API key and Digit.ink connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Issuer Profile



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digitink/latest/actions/get-issuer-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digitink/latest/actions/get-issuer-profile?${params}`, {
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
      "@context": [
        "string"
      ],
      "description": "string",
      "email": "ava@example.com",
      "id": "string",
      "image": "string",
      "name": "Ava Chen",
      "publicKey": [
        {}
      ],
      "revocationList": "string",
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Get Issuer Profile action reference](actions/get-issuer-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/digitink/latest/actions/get-issuer-profile).

## Add Batch To Stack



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/digitink/latest/actions/add-batch-to-stack" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "stackUuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/digitink/latest/actions/add-batch-to-stack', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "stackUuid": "string"
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
      "batchIds": [
        "string"
      ],
      "issuerUri": "string",
      "stackName": "Ava Chen",
      "stackUuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Batch To Stack action reference](actions/add-batch-to-stack.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/digitink/latest/actions/add-batch-to-stack).
