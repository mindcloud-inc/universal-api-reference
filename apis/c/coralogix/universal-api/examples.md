# Coralogix Universal API Examples

These examples use the MindCloud API key and Coralogix connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List System Roles



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coralogix/latest/actions/list-system-roles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coralogix/latest/actions/list-system-roles?${params}`, {
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
      "roles": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List System Roles action reference](actions/list-system-roles.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/coralogix/latest/actions/list-system-roles).
