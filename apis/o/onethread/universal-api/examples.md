# Onethread Universal API Examples

These examples use the MindCloud API key and Onethread connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User Meta Data



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onethread/latest/actions/get-user-meta-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onethread/latest/actions/get-user-meta-data?${params}`, {
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
      "accounts": [
        {}
      ],
      "companies": [
        {}
      ],
      "favouriteProjectLists": [
        {}
      ],
      "labels": [
        {}
      ],
      "projects": [
        {}
      ],
      "statuses": [
        {}
      ],
      "taskAssigns": [
        {}
      ],
      "taskLabels": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get User Meta Data action reference](actions/get-user-meta-data.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/onethread/latest/actions/get-user-meta-data).

## Get Auth Token (Email and Password)



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/onethread/latest/actions/get-auth-token-email-and-password" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/onethread/latest/actions/get-auth-token-email-and-password', {
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
      "refreshToken": "string",
      "success": true,
      "user": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Auth Token (Email and Password) action reference](actions/get-auth-token-email-and-password.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/onethread/latest/actions/get-auth-token-email-and-password).
