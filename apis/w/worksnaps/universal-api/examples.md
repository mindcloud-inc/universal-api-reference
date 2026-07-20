# Worksnaps Universal API Examples

These examples use the MindCloud API key and Worksnaps connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user from Worksnaps.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/get-current-user?${params}`, {
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
      "api_token": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": 1,
      "is_in_daylight_time": true,
      "last_name": "Chen",
      "login": "string",
      "timezone_id": 1,
      "timezone_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/worksnaps/latest/actions/get-current-user).

## Create a new project

Creates a new project in Worksnaps.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/create-a-new-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": "<project><name>MindCloud Validator Project</name><description>Validator fixture project for Worksnaps app build.</description></project>"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/create-a-new-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": "<project><name>MindCloud Validator Project</name><description>Validator fixture project for Worksnaps app build.</description></project>"
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
      "description": "string",
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Create a new project action reference](actions/create-a-new-project.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/worksnaps/latest/actions/create-a-new-project).
