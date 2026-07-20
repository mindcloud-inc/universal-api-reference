# Craftboxx Universal API Examples

These examples use the MindCloud API key and Craftboxx connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Employees

Returns employees from Craftboxx.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/craftboxx/latest/actions/list-employees?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/craftboxx/latest/actions/list-employees?${params}`, {
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
      "city": "string",
      "color": "string",
      "contrast_color": "string",
      "country": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "department": "string",
      "driver_license": true,
      "email": "ava@example.com",
      "first_line": "string",
      "first_name": "Ava",
      "full_name": "Ava Chen",
      "group_id": 1,
      "holidays_overtake_balances": true,
      "holidays_per_year": 1,
      "icon": "string",
      "id": 1,
      "inactive": true,
      "info": "string",
      "initials": "string",
      "interfaces": [
        "string"
      ],
      "last_name": "Chen",
      "locale": "string",
      "mobile": "string",
      "number": "string",
      "phone": "string",
      "picture_is_avatar": true,
      "planner_changelog_url": "https://example.com",
      "planner_delete_url": "https://example.com",
      "planner_details_url": "https://example.com",
      "planner_edit_url": "https://example.com",
      "position": "string",
      "skills": "string",
      "sort_order": 1,
      "street": "string",
      "timezone": "string",
      "truck_license": true,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Employees action reference](actions/list-employees.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/craftboxx/latest/actions/list-employees).

## Create Access Token

Creates and returns a Craftboxx access token.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/craftboxx/latest/actions/create-access-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "{{credentials.email}}"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/craftboxx/latest/actions/create-access-token', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "{{credentials.email}}"
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
      "access_token": "string",
      "token_type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Access Token action reference](actions/create-access-token.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/craftboxx/latest/actions/create-access-token).
