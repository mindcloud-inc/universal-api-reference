# Moblico Universal API Examples

These examples use the MindCloud API key and Moblico connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check User Exists



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moblico/latest/actions/check-user-exists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moblico/latest/actions/check-user-exists?${params}`, {
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
      "message": "string",
      "statusType": 1
    }
  ],
  "meta": {}
}
```

See the full [Check User Exists action reference](actions/check-user-exists.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/moblico/latest/actions/check-user-exists).
