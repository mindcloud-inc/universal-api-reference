# Kladana Universal API Examples

These examples use the MindCloud API key and Kladana connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current Employee Context

Retrieves current employee context from Kladana.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kladana/latest/actions/get-current-employee-context?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kladana/latest/actions/get-current-employee-context?${params}`, {
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
      "archived": true,
      "created": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "id": "string",
      "lastName": "Chen",
      "login": "string",
      "meta": {},
      "name": "Ava Chen",
      "phone": "string",
      "position": "string",
      "uid": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Get Current Employee Context action reference](actions/get-current-employee-context.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/kladana/latest/actions/get-current-employee-context).
