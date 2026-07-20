# ProxiedMail Universal API Examples

These examples use the MindCloud API key and ProxiedMail connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Proxy Bindings



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/proxiedMail/latest/actions/list-proxy-bindings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/proxiedMail/latest/actions/list-proxy-bindings?${params}`, {
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
      "attributes": {
        "callbackUrl": "https://example.com",
        "createdAt": "string",
        "deliveryMethod": 1,
        "description": "string",
        "isBrowsable": true,
        "proxyAddress": "string",
        "realAddresses": {
          "apps@mindcloud": {
            "co": {
              "confirmationRequestShown": true,
              "isEnabled": true,
              "isVerified": true,
              "verificationType": 1
            }
          }
        },
        "receivedEmails": 1,
        "type": 1,
        "updatedAt": "string",
        "wildcardAutoCreateOn": {}
      },
      "id": "string",
      "relationships": {
        "user": {
          "data": {
            "id": "string",
            "type": "string"
          }
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Proxy Bindings action reference](actions/list-proxy-bindings.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/proxiedMail/latest/actions/list-proxy-bindings).

## Authenticate With Username And Password



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/proxiedMail/latest/actions/authenticate-with-username-and-password" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "username": "apps@mindcloud.co",
  "password": "account password"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/proxiedMail/latest/actions/authenticate-with-username-and-password', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "username": "apps@mindcloud.co",
    "password": "account password"
  })
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

See the full [Authenticate With Username And Password action reference](actions/authenticate-with-username-and-password.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/proxiedMail/latest/actions/authenticate-with-username-and-password).
