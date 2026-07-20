# DateX Universal API Examples

These examples use the MindCloud API key and DateX connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Echo Test



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dateXNew/latest/actions/echo-test?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dateXNew/latest/actions/echo-test?${params}`, {
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
      "greeting": "string"
    }
  ],
  "meta": {}
}
```

See the full [Echo Test action reference](actions/echo-test.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dateXNew/latest/actions/echo-test).

## Authorize



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dateXNew/latest/actions/authorize" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dateXNew/latest/actions/authorize', {
  method: 'POST',
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
      "accessToken": "string",
      "expiresIn": 1,
      "extExpiresIn": 1,
      "tokenType": "string"
    }
  ],
  "meta": {}
}
```

See the full [Authorize action reference](actions/authorize.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dateXNew/latest/actions/authorize).
