# Google Groups Universal API Examples

These examples use the MindCloud API key and Google Groups connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Groups

Retrieves groups from Google Groups for a domain or user.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleGroups/latest/actions/list-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleGroups/latest/actions/list-groups?${params}`, {
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
      "adminCreated": true,
      "description": "string",
      "directMembersCount": "string",
      "email": "ava@example.com",
      "etag": "string",
      "id": "string",
      "kind": "string",
      "name": "Ava Chen",
      "nonEditableAliases": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Groups action reference](actions/list-groups.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/googleGroups/latest/actions/list-groups).

## Add Group Member

Adds a member to a group in Google Groups.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleGroups/latest/actions/add-group-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupKey": "string",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleGroups/latest/actions/add-group-member', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupKey": "string",
    "email": "ava@example.com"
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
      "deliverySettings": "string",
      "email": "ava@example.com",
      "etag": "string",
      "id": "string",
      "kind": "string",
      "role": "string",
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Group Member action reference](actions/add-group-member.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/googleGroups/latest/actions/add-group-member).
