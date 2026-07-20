# Cloze Universal API Examples

These examples use the MindCloud API key and Cloze connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User Profile

Retrieves a user profile from Cloze.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloze/latest/actions/get-user-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloze/latest/actions/get-user-profile?${params}`, {
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
      "country": "string",
      "email": "ava@example.com",
      "first": "string",
      "key": "string",
      "last": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get User Profile action reference](actions/get-user-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cloze/latest/actions/get-user-profile).

## Add Communication Record

Creates a communication record in Cloze.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cloze/latest/actions/add-communication-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloze/latest/actions/add-communication-record', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "errorcode": 1
    }
  ],
  "meta": {}
}
```

See the full [Add Communication Record action reference](actions/add-communication-record.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cloze/latest/actions/add-communication-record).
