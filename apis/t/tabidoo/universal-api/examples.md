# Tabidoo Universal API Examples

These examples use the MindCloud API key and Tabidoo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Apps

Retrieves applications from a Tabidoo workspace.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tabidoo/latest/actions/list-apps?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tabidoo/latest/actions/list-apps?${params}`, {
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
      "id": "string",
      "internalName": "Ava Chen",
      "isMultiLanguage": true,
      "name": "Ava Chen",
      "namesI18n": {
        "en": "Ava Chen"
      },
      "timeZone": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Apps action reference](actions/list-apps.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tabidoo/latest/actions/list-apps).

## Create Development App From Production App

Creates a development app from a production app in Tabidoo.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tabidoo/latest/actions/create-development-app-from-production-app" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "applicationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tabidoo/latest/actions/create-development-app-from-production-app', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "applicationId": "string"
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

See the full [Create Development App From Production App action reference](actions/create-development-app-from-production-app.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tabidoo/latest/actions/create-development-app-from-production-app).
