# Florm Universal API Examples

These examples use the MindCloud API key and Florm connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get My Profile

Retrieves your user profile from Florm.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/florm/latest/actions/get-my-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/florm/latest/actions/get-my-profile?${params}`, {
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
      "email": "ava@example.com",
      "guid": "string",
      "isActive": true,
      "name": "Ava Chen",
      "settings": {
        "language": "string",
        "notificationsEvents": true,
        "notificationsNews": true
      }
    }
  ],
  "meta": {}
}
```

See the full [Get My Profile action reference](actions/get-my-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/florm/latest/actions/get-my-profile).

## Copy Form

Creates a copy of a Florm form.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/florm/latest/actions/copy-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formGuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/florm/latest/actions/copy-form', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formGuid": "string"
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
      "createdAt": "string",
      "designThemeGuid": "string",
      "guid": "string",
      "settings": {},
      "sharedGuid": "string",
      "slug": "string",
      "steps": [
        {}
      ],
      "updatedAt": "string",
      "urlParameters": {},
      "version": 1,
      "workspaceGuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Copy Form action reference](actions/copy-form.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/florm/latest/actions/copy-form).
