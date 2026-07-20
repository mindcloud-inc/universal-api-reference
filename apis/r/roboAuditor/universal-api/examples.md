# RoboAuditor Universal API Examples

These examples use the MindCloud API key and RoboAuditor connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check URL Exists



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/roboAuditor/latest/actions/check-url-exists?connectionId=$CONNECTION_ID&websiteUrl=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "websiteUrl": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/roboAuditor/latest/actions/check-url-exists?${params}`, {
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
      "exist": "string"
    }
  ],
  "meta": {}
}
```

See the full [Check URL Exists action reference](actions/check-url-exists.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/roboAuditor/latest/actions/check-url-exists).

## Authenticate



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/roboAuditor/latest/actions/authenticate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "{{credentials.email}}"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/roboAuditor/latest/actions/authenticate', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "{{credentials.email}}"
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
      "access_token": "string",
      "expires_in": 1,
      "refresh_token": "string",
      "token_type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Authenticate action reference](actions/authenticate.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/roboAuditor/latest/actions/authenticate).
