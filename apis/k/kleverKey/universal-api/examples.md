# KleverKey Universal API Examples

These examples use the MindCloud API key and KleverKey connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kleverKey/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kleverKey/latest/actions/get-current-user?${params}`, {
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
      "accessGroups": [
        {}
      ],
      "cultureCode": "string",
      "displayName": "Ava Chen",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "organizationIds": [
        1
      ],
      "roles": [
        {}
      ],
      "type": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/kleverKey/latest/actions/get-current-user).

## Add Access Group



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kleverKey/latest/actions/add-access-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": 1,
  "name": "Ava Chen",
  "lockIds[]": [
    1
  ],
  "userIds[]": [
    1
  ],
  "permissionType": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kleverKey/latest/actions/add-access-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": 1,
    "name": "Ava Chen",
    "lockIds[]": [1],
    "userIds[]": [1],
    "permissionType": 1
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
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "dateUpdated": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "locks": [
        {}
      ],
      "name": "Ava Chen",
      "organizationId": 1,
      "permissionType": 1,
      "users": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Add Access Group action reference](actions/add-access-group.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/kleverKey/latest/actions/add-access-group).
