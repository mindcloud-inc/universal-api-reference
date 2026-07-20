# Themeforest Universal API Examples

These examples use the MindCloud API key and Themeforest connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Email

Retrieves the connected Envato account email.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/themeForest/latest/actions/get-account-email?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/themeForest/latest/actions/get-account-email?${params}`, {
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
      "email": "ava@example.com"
    }
  ],
  "meta": {}
}
```

See the full [Get Account Email action reference](actions/get-account-email.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/themeForest/latest/actions/get-account-email).
