# Scalelist Universal API Examples

These examples use the MindCloud API key and Scalelist connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Find Email

Finds a contact email in Scalelist.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scalelist/latest/actions/find-email?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scalelist/latest/actions/find-email?${params}`, {
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
      "_id": "string",
      "companyDomain": "string",
      "email": "ava@example.com",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Find Email action reference](actions/find-email.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/scalelist/latest/actions/find-email).
