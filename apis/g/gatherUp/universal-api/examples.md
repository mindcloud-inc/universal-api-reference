# GatherUp Universal API Examples

These examples use the MindCloud API key and GatherUp connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Businesses

Retrieves a list of businesses from GatherUp.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/list-businesses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/list-businesses?${params}`, {
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
      "businessCity": "string",
      "businessCountry": "string",
      "businessDeleted": 1,
      "businessId": 1,
      "businessName": "Ava Chen",
      "businessOrganisationType": "string",
      "businessPackage": "string",
      "businessPhone": "string",
      "businessState": "string",
      "businessStreetAddress": "string",
      "businessWebsiteURL": "https://example.com",
      "businessZip": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Businesses action reference](actions/list-businesses.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gatherUp/latest/actions/list-businesses).

## Add Email to Receive Notifications

Adds a notification email address in GatherUp.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/add-email-to-receive-notifications" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "businessId": 1,
  "email": "ava@example.com",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/add-email-to-receive-notifications', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "businessId": 1,
    "email": "ava@example.com",
    "type": "string"
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
      "errorCode": 1,
      "errorMessage": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Email to Receive Notifications action reference](actions/add-email-to-receive-notifications.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gatherUp/latest/actions/add-email-to-receive-notifications).
