# Devin Universal API Examples

These examples use the MindCloud API key and Devin connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Self

Retrieves the authenticated user from Devin.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/devin/latest/actions/get-self?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/devin/latest/actions/get-self?${params}`, {
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
      "org_id": "string",
      "principal_type": "string",
      "service_user_id": "string",
      "service_user_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Self action reference](actions/get-self.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/devin/latest/actions/get-self).

## Append Session Tags

Updates session tags by appending new tags in Devin.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/devin/latest/actions/append-session-tags" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "devinId": "string",
  "orgId": "string",
  "tags[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/devin/latest/actions/append-session-tags', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "devinId": "string",
    "orgId": "string",
    "tags[]": ["string"]
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
      "tags": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Append Session Tags action reference](actions/append-session-tags.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/devin/latest/actions/append-session-tags).
