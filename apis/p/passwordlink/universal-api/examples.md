# Password.link Universal API Examples

These examples use the MindCloud API key and Password.link connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Secrets



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/passwordlink/latest/actions/list-secrets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/passwordlink/latest/actions/list-secrets?${params}`, {
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
      "captcha": true,
      "createdAt": "string",
      "description": "string",
      "expiration": 1,
      "expired": true,
      "id": "string",
      "maxViews": 1,
      "message": "string",
      "password": true,
      "viewButton": true,
      "views": [
        {}
      ],
      "viewTimes": 1
    }
  ],
  "meta": {}
}
```

See the full [List Secrets action reference](actions/list-secrets.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/passwordlink/latest/actions/list-secrets).

## Create Secret



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/passwordlink/latest/actions/create-secret" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ciphertext": "string",
  "passwordPartPrivate": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/passwordlink/latest/actions/create-secret', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ciphertext": "string",
    "passwordPartPrivate": "string"
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
      "id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Secret action reference](actions/create-secret.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/passwordlink/latest/actions/create-secret).
