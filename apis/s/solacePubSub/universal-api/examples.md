# Solace PubSub+ Universal API Examples

These examples use the MindCloud API key and Solace PubSub+ connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get API Tokens

Retrieves API tokens from Solace PubSub+.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/solacePubSub/latest/actions/get-api-tokens?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/solacePubSub/latest/actions/get-api-tokens?${params}`, {
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
      "id": "string",
      "name": "Ava Chen",
      "organizationId": "string",
      "permissions": [
        "string"
      ],
      "resourceAssignments": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get API Tokens action reference](actions/get-api-tokens.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/solacePubSub/latest/actions/get-api-tokens).
