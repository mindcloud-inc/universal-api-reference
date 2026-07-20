# IgniSign Universal API Examples

These examples use the MindCloud API key and IgniSign connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Application Context



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/igniSign/latest/actions/get-application-context?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/igniSign/latest/actions/get-application-context?${params}`, {
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
      "_createdAt": "string",
      "appId": "string",
      "appName": "Ava Chen",
      "appType": "string",
      "config": {},
      "envSettings": {},
      "ignisignApiVersion": "string",
      "orgId": "string",
      "settings": {},
      "signatureProfiles": {},
      "signerProfiles": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Application Context action reference](actions/get-application-context.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/igniSign/latest/actions/get-application-context).

## Close Signature Request



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/igniSign/latest/actions/close-signature-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "signatureRequestId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/igniSign/latest/actions/close-signature-request', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "signatureRequestId": "string"
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
      "signatureRequestId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Close Signature Request action reference](actions/close-signature-request.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/igniSign/latest/actions/close-signature-request).
