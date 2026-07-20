# Dynosend Universal API Examples

These examples use the MindCloud API key and Dynosend connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check Blacklist

Checks whether a contact is blacklisted in Dynosend.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dynosend/latest/actions/check-blacklist?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dynosend/latest/actions/check-blacklist?${params}`, {
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
      "blacklist_time": "2026-05-07T12:00:00.000Z",
      "blacklisted": true,
      "email": "ava@example.com",
      "reason": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Check Blacklist action reference](actions/check-blacklist.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dynosend/latest/actions/check-blacklist).

## Add Contact Tags by Email

Adds tags to a Dynosend contact by email address.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dynosend/latest/actions/add-contact-tags-by-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "audienceUid": "string",
  "email": "ava@example.com",
  "tag": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dynosend/latest/actions/add-contact-tags-by-email', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "audienceUid": "string",
    "email": "ava@example.com",
    "tag": "string"
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

See the full [Add Contact Tags by Email action reference](actions/add-contact-tags-by-email.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dynosend/latest/actions/add-contact-tags-by-email).
