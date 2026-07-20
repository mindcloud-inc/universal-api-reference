# ServerAvatar Universal API Examples

These examples use the MindCloud API key and ServerAvatar connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Organizations

Retrieves organizations from ServerAvatar.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/list-organizations?${params}`, {
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
      "organizations": [
        {
          "createdAt": "string",
          "id": 1,
          "members": [
            {
              "avatar": "string",
              "email": "ava@example.com",
              "name": "Ava Chen",
              "roles": [
                {
                  "id": 1,
                  "role": "string"
                }
              ]
            }
          ],
          "name": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Organizations action reference](actions/list-organizations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/serverAvatar/latest/actions/list-organizations).
