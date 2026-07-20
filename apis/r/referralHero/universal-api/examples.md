# ReferralHero Universal API Examples

These examples use the MindCloud API key and ReferralHero connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Lists

Retrieves lists from ReferralHero.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/referralHero/latest/actions/list-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/referralHero/latest/actions/list-lists?${params}`, {
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
      "createdAt": 1,
      "name": "Ava Chen",
      "response": "string",
      "subscribers": 1,
      "type": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Lists action reference](actions/list-lists.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/referralHero/latest/actions/list-lists).

## Add Subscriber

Creates a new subscriber in ReferralHero.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/referralHero/latest/actions/add-subscriber" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "uuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/referralHero/latest/actions/add-subscriber', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "uuid": "string"
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
      "code": "string",
      "createdAt": 1,
      "email": "ava@example.com",
      "id": "string",
      "lastUpdatedAt": 1,
      "name": "Ava Chen",
      "response": "string",
      "universalLink": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Add Subscriber action reference](actions/add-subscriber.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/referralHero/latest/actions/add-subscriber).
