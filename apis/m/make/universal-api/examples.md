# Make Universal API Examples

These examples use the MindCloud API key and Make connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current Authorization

Returns current authorization details for the authenticated user, including the token scopes and authentication method used.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/make/latest/actions/get-current-authorization?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/make/latest/actions/get-current-authorization?${params}`, {
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
      "authUsed": "string",
      "scope": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get Current Authorization action reference](actions/get-current-authorization.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/make/latest/actions/get-current-authorization).

## Create Scenario Folder

Creates a scenario folder in the specified team.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/make/latest/actions/create-scenario-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamId": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/make/latest/actions/create-scenario-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamId": 1,
    "name": "Ava Chen"
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
      "id": 1,
      "name": "Ava Chen",
      "scenariosTotal": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Scenario Folder action reference](actions/create-scenario-folder.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/make/latest/actions/create-scenario-folder).
