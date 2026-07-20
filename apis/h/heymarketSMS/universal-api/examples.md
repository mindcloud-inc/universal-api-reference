# Heymarket SMS Universal API Examples

These examples use the MindCloud API key and Heymarket SMS connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Contact



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/get-contact?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/get-contact?${params}`, {
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
      "assigned_user_id": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "creator_id": 1,
      "display_name": "Ava Chen",
      "email": "ava@example.com",
      "first": "string",
      "id": 1,
      "last": "string",
      "op": "string",
      "phone": "string",
      "rev": 1,
      "shared": true,
      "team_id": 1,
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Get Contact action reference](actions/get-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/heymarketSMS/latest/actions/get-contact).

## Batch Create Contacts



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/batch-create-contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contacts[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/batch-create-contacts', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contacts[]": [{}]
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
      "response": "string"
    }
  ],
  "meta": {}
}
```

See the full [Batch Create Contacts action reference](actions/batch-create-contacts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/heymarketSMS/latest/actions/batch-create-contacts).
