# MailerLite Universal API Examples

These examples use the MindCloud API key and MailerLite connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Subscribers

Retrieves a page of subscribers from MailerLite.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/list-subscribers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/list-subscribers?${params}`, {
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
      "clickRate": 1,
      "clicksCount": 1,
      "createdAt": "string",
      "email": "ava@example.com",
      "fields": {
        "city": {},
        "company": {},
        "country": {},
        "lastName": {},
        "mcField20260302202529": {},
        "mcField20260302202809": {},
        "mcField20260302203026": {},
        "mcField20260302203214": {},
        "mcField20260302203521": {},
        "mcField20260302203754": {},
        "mcField20260302204008": {},
        "mcField20260302204855": {},
        "name": {},
        "phone": {},
        "state": {},
        "zIP": {}
      },
      "id": "string",
      "ipAddress": {},
      "openRate": 1,
      "opensCount": 1,
      "optedInAt": {},
      "optinIp": {},
      "sent": 1,
      "source": "string",
      "status": "string",
      "subscribedAt": "string",
      "unsubscribedAt": {},
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Subscribers action reference](actions/list-subscribers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mailerLite/latest/actions/list-subscribers).

## Assign Subscriber to Group

Assigns an existing subscriber to a group in MailerLite.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/assign-subscriber-to-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subscriber_id": "180863157267334516",
  "group_id": "180900000000000001"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/assign-subscriber-to-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subscriber_id": "180863157267334516",
    "group_id": "180900000000000001"
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
      "activeCount": 1,
      "bouncedCount": 1,
      "clickRate": {},
      "clicksCount": 1,
      "createdAt": "string",
      "id": "string",
      "junkCount": 1,
      "name": "Ava Chen",
      "openRate": {},
      "opensCount": 1,
      "sentCount": 1,
      "unconfirmedCount": 1,
      "unsubscribedCount": 1
    }
  ],
  "meta": {}
}
```

See the full [Assign Subscriber to Group action reference](actions/assign-subscriber-to-group.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mailerLite/latest/actions/assign-subscriber-to-group).
