# Convert Universal API Examples

These examples use the MindCloud API key and Convert connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List API Keys

Retrieves API keys from Convert for an account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/convert/latest/actions/list-api-keys?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/convert/latest/actions/list-api-keys?${params}`, {
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
      "auth_type": "string",
      "key_id": "string",
      "key_secret": "string",
      "name": "Ava Chen",
      "projects": [
        1
      ],
      "role": "string"
    }
  ],
  "meta": {}
}
```

See the full [List API Keys action reference](actions/list-api-keys.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/convert/latest/actions/list-api-keys).
