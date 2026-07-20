# Deepset Universal API Examples

These examples use the MindCloud API key and Deepset connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Read Current User

Retrieves the current user from Deepset.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepset/latest/actions/read-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepset/latest/actions/read-current-user?${params}`, {
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
      "deleted": true,
      "email": "ava@example.com",
      "family_name": "Ava Chen",
      "given_name": "Ava Chen",
      "oauth_id": "string",
      "oauth_provider": "string",
      "organization": {
        "gpu_enabled": true,
        "local_builder_enabled": true,
        "max_workspaces": 1,
        "name": "Ava Chen",
        "organization_id": "string",
        "organization_type": "string",
        "role": "string",
        "workspaces": [
          {
            "name": "Ava Chen",
            "role": "string",
            "role_id": "string"
          }
        ]
      },
      "user_id": "string",
      "userflow_signature": "string"
    }
  ],
  "meta": {}
}
```

See the full [Read Current User action reference](actions/read-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/deepset/latest/actions/read-current-user).
