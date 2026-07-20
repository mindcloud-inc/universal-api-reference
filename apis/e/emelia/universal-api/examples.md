# Emelia Universal API Examples

These examples use the MindCloud API key and Emelia connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User Data

Retrieves user account data from Emelia.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emelia/latest/actions/get-user-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emelia/latest/actions/get-user-data?${params}`, {
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
      "data": {
        "me": {
          "dueInvoice": {},
          "email": "ava@example.com",
          "joinedDate": "2026-05-07T12:00:00.000Z",
          "name": "Ava Chen",
          "picture": {},
          "showMailbox": {},
          "uid": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

See the full [Get User Data action reference](actions/get-user-data.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/emelia/latest/actions/get-user-data).

## Add Contact To Campaign

Adds a contact to a campaign in Emelia.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/emelia/latest/actions/add-contact-to-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contact": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/emelia/latest/actions/add-contact-to-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contact": "string",
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
      "data": {
        "addContactToCampaignHook": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Add Contact To Campaign action reference](actions/add-contact-to-campaign.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/emelia/latest/actions/add-contact-to-campaign).
