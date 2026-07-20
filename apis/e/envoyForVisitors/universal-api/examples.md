# Envoy for Visitors Universal API Examples

These examples use the MindCloud API key and Envoy for Visitors connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Locations

Retrieves locations from Envoy for Visitors.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/envoyForVisitors/latest/actions/list-locations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/envoyForVisitors/latest/actions/list-locations?${params}`, {
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
      "address": {},
      "capacityLimit": 1,
      "companyId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "enabled": true,
      "id": "string",
      "locale": "string",
      "logoUrl": "https://example.com",
      "name": "Ava Chen",
      "scheduleAheadLimit": 1,
      "timezone": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Locations action reference](actions/list-locations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/envoyForVisitors/latest/actions/list-locations).

## Check In Invite

Checks in a visitor from an invite in Envoy for Visitors.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/envoyForVisitors/latest/actions/check-in-invite" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/envoyForVisitors/latest/actions/check-in-invite', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
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
      "agreementsStatus": "string",
      "customFields": [
        {}
      ],
      "email": "ava@example.com",
      "flowId": "string",
      "fullName": "Ava Chen",
      "id": "string",
      "isDelivery": true,
      "locationId": "string",
      "signedInAt": "2026-05-07T12:00:00.000Z",
      "signedInVia": "string",
      "signedOutAt": "2026-05-07T12:00:00.000Z",
      "signedOutVia": "string"
    }
  ],
  "meta": {}
}
```

See the full [Check In Invite action reference](actions/check-in-invite.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/envoyForVisitors/latest/actions/check-in-invite).
