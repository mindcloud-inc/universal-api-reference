# Notifyre SMS Universal API Examples

These examples use the MindCloud API key and Notifyre SMS connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Download MMS Reply

Downloads an MMS reply attachment from Notifyre.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/download-mms-reply?connectionId=$CONNECTION_ID&replyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "replyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/download-mms-reply?${params}`, {
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
      "content": "string"
    }
  ],
  "meta": {}
}
```

See the full [Download MMS Reply action reference](actions/download-mms-reply.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/notifyreSMS/latest/actions/download-mms-reply).

## Add Contacts To Groups

Adds contacts to groups in Notifyre.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/add-contacts-to-groups" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contacts": "string",
  "groups": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/add-contacts-to-groups', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contacts": "string",
    "groups": "string"
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
      "added": true
    }
  ],
  "meta": {}
}
```

See the full [Add Contacts To Groups action reference](actions/add-contacts-to-groups.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/notifyreSMS/latest/actions/add-contacts-to-groups).
