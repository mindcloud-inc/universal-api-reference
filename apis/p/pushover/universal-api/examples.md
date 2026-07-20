# Pushover Universal API Examples

These examples use the MindCloud API key and Pushover connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Validate User or Group



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pushover/latest/actions/validate-user-or-group?connectionId=$CONNECTION_ID&user=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "user": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pushover/latest/actions/validate-user-or-group?${params}`, {
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
      "devices": [
        "string"
      ],
      "group": 1,
      "licenses": [
        "string"
      ],
      "request": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

See the full [Validate User or Group action reference](actions/validate-user-or-group.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pushover/latest/actions/validate-user-or-group).

## Add User to Group



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pushover/latest/actions/add-user-to-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "group": "string",
  "user": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pushover/latest/actions/add-user-to-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "group": "string",
    "user": "string"
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
      "request": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

See the full [Add User to Group action reference](actions/add-user-to-group.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pushover/latest/actions/add-user-to-group).
