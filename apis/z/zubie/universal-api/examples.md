# Zubie Universal API Examples

These examples use the MindCloud API key and Zubie connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User Profile

Retrieves the current user profile from Zubie.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zubie/latest/actions/get-current-user-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zubie/latest/actions/get-current-user-profile?${params}`, {
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
      "account_key": "string",
      "account_role": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "key": "string",
      "last_name": "Chen",
      "preferred_locale": "string",
      "updated": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User Profile action reference](actions/get-current-user-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zubie/latest/actions/get-current-user-profile).

## Apply Group Memberships

Applies group memberships in Zubie.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zubie/latest/actions/apply-group-memberships" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "action": "string",
  "group_keys[]": [
    "string"
  ],
  "member_keys[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zubie/latest/actions/apply-group-memberships', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "action": "string",
    "group_keys[]": ["string"],
    "member_keys[]": ["string"]
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "action": "string",
      "group_keys": [
        "string"
      ],
      "member_keys": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Apply Group Memberships action reference](actions/apply-group-memberships.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zubie/latest/actions/apply-group-memberships).
