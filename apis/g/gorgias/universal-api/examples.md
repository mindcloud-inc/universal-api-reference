# Gorgias Universal API Examples

These examples use the MindCloud API key and Gorgias connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Retrieve Account

Retrieves account details from Gorgias.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gorgias/latest/actions/retrieve-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gorgias/latest/actions/retrieve-account?${params}`, {
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
      "created_datetime": "string",
      "current_subscription": {},
      "deactivated_datetime": "string",
      "domain": "string",
      "meta": {},
      "settings": [
        {}
      ],
      "status": {}
    }
  ],
  "meta": {}
}
```

See the full [Retrieve Account action reference](actions/retrieve-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gorgias/latest/actions/retrieve-account).
