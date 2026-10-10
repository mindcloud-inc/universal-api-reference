# Apollo Universal API Examples

These examples use the MindCloud API key and Apollo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User Profile Info

Retrieves the authorized user profile from Apollo.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/get-user-profile-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/get-user-profile-info?${params}`, {
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
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "teamId": "string",
      "title": {}
    }
  ],
  "meta": {}
}
```

See the full [Get User Profile Info action reference](actions/get-user-profile-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/apolloio/latest/actions/get-user-profile-info).

## Add Records to a List



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/add-records-to-a-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "entityIds[]": [
    "string"
  ],
  "labelNames[]": [
    "Ava Chen"
  ],
  "modality": "accounts"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/add-records-to-a-list', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "entityIds[]": ["string"],
    "labelNames[]": ["Ava Chen"],
    "modality": "accounts"
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
      "cachedCount": 1,
      "createdAt": "string",
      "id": "string",
      "modality": "string",
      "name": "Ava Chen",
      "updatedAt": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Records to a List action reference](actions/add-records-to-a-list.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/apolloio/latest/actions/add-records-to-a-list).
