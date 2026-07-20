# Certifier Universal API Examples

These examples use the MindCloud API key and Certifier connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Credential

Retrieves detailed credential information from Certifier.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/certifier/latest/actions/get-credential?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/certifier/latest/actions/get-credential?${params}`, {
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
      "attributes": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customAttributes": {},
      "expiryDate": "2026-05-07T12:00:00.000Z",
      "groupId": "string",
      "id": "string",
      "issueDate": "2026-05-07T12:00:00.000Z",
      "publicId": "string",
      "recipient": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      },
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Get Credential action reference](actions/get-credential.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/certifier/latest/actions/get-credential).

## Create Credential

Creates a new credential in Certifier.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/certifier/latest/actions/create-credential" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "group_id": "string",
  "recipient": {},
  "recipient.name": "Ava Chen",
  "recipient.email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/certifier/latest/actions/create-credential', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "group_id": "string",
    "recipient": {},
    "recipient.name": "Ava Chen",
    "recipient.email": "ava@example.com"
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
      "attributes": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customAttributes": {},
      "expiryDate": "2026-05-07T12:00:00.000Z",
      "groupId": "string",
      "id": "string",
      "issueDate": "2026-05-07T12:00:00.000Z",
      "publicId": "string",
      "recipient": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      },
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Create Credential action reference](actions/create-credential.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/certifier/latest/actions/create-credential).
