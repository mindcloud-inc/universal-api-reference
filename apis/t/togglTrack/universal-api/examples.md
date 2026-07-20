# Toggl Track Universal API Examples

These examples use the MindCloud API key and Toggl Track connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user from Toggl Track.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/get-current-user?${params}`, {
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
      "apiToken": "string",
      "at": "string",
      "authorizationUpdatedAt": "string",
      "beginningOfWeek": 1,
      "countryId": 1,
      "createdAt": "string",
      "defaultWorkspaceId": 1,
      "email": "ava@example.com",
      "fullname": "Ava Chen",
      "hasPassword": true,
      "id": 1,
      "imageUrl": "https://example.com",
      "oauthProviders": [
        "string"
      ],
      "openidEmail": {},
      "openidEnabled": true,
      "timezone": "string",
      "togglAccountsId": "string",
      "twoFaEnabled": true,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/togglTrack/latest/actions/get-current-user).

## Archive Client

Archives an existing client in Toggl Track.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/archive-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": 1,
  "clientId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/archive-client', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": 1,
    "clientId": 1
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
      "value": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Archive Client action reference](actions/archive-client.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/togglTrack/latest/actions/archive-client).
