# Perfit Universal API Examples

These examples use the MindCloud API key and Perfit connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Account Activity



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/perfit/latest/actions/list-account-activity?connectionId=$CONNECTION_ID&account=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "account": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/perfit/latest/actions/list-account-activity?${params}`, {
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
      "account": "string",
      "batch_id": "string",
      "custom_args": {},
      "day_of_week": 1,
      "domain": "string",
      "email": "ava@example.com",
      "hour_of_day": 1,
      "mail_id": "string",
      "mail_type": "string",
      "mta": "string",
      "sent_timestamp": "2026-05-07T12:00:00.000Z",
      "tags": [
        "string"
      ],
      "timestamp": "2026-05-07T12:00:00.000Z",
      "track_id": "string",
      "track_type": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Account Activity action reference](actions/list-account-activity.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/perfit/latest/actions/list-account-activity).

## Add Interest To Contact



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/perfit/latest/actions/add-interest-to-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "account": "string",
  "contactId": "string",
  "interest": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/perfit/latest/actions/add-interest-to-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "account": "string",
    "contactId": "string",
    "interest": "string"
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
      "id": 1,
      "name": "Ava Chen",
      "subscribed": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Add Interest To Contact action reference](actions/add-interest-to-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/perfit/latest/actions/add-interest-to-contact).
