# Instabot Universal API Examples

These examples use the MindCloud API key and Instabot connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Application Info

Retrieves application details from Instabot.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instabot/latest/actions/get-application-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instabot/latest/actions/get-application-info?${params}`, {
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
      "agencyId": 1,
      "applicationName": "Ava Chen",
      "devCompanyId": 1,
      "hideBrandedFooterInChat": true,
      "version": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Application Info action reference](actions/get-application-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/instabot/latest/actions/get-application-info).

## Create User

Creates a new user in Instabot.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/instabot/latest/actions/create-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "username": "Ava Chen",
  "userpassword": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instabot/latest/actions/create-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "username": "Ava Chen",
    "userpassword": "string"
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
      "objectId": 1
    }
  ],
  "meta": {}
}
```

See the full [Create User action reference](actions/create-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/instabot/latest/actions/create-user).
