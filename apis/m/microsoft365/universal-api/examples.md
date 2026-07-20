# Microsoft 365 Universal API Examples

These examples use the MindCloud API key and Microsoft 365 connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get My Profile

Retrieves your Microsoft 365 profile.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/get-my-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/get-my-profile?${params}`, {
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
      "businessPhones": [
        "string"
      ],
      "displayName": "Ava Chen",
      "givenName": "Ava Chen",
      "id": "string",
      "jobTitle": "string",
      "mail": "string",
      "mobilePhone": "string",
      "officeLocation": "string",
      "preferredLanguage": "string",
      "surname": "Ava Chen",
      "userPrincipalName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get My Profile action reference](actions/get-my-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/microsoft365/latest/actions/get-my-profile).

## Accept Event

Accepts an event in Microsoft 365.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/accept-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventId": "AAMkAG..."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/accept-event', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventId": "AAMkAG..."
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

See the full [Accept Event action reference](actions/accept-event.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/microsoft365/latest/actions/accept-event).
