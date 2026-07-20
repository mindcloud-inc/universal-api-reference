# DeskTime Universal API Examples

These examples use the MindCloud API key and DeskTime connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Company Account

Retrieves your company account details from DeskTime.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deskTime/latest/actions/get-company-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deskTime/latest/actions/get-company-account?${params}`, {
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
      "__request_time": "string",
      "name": "Ava Chen",
      "timezone_identifier": "string",
      "work_duration": "string",
      "work_ends": "string",
      "work_start_tracking": "string",
      "work_starts": "string",
      "work_stop_tracking": "string",
      "working_days": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Company Account action reference](actions/get-company-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/deskTime/latest/actions/get-company-account).

## Create Project

Creates a new project in DeskTime with an optional task.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/deskTime/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project": "MindCloud Sandbox"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deskTime/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project": "MindCloud Sandbox"
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
      "__request_time": "string",
      "project": {}
    }
  ],
  "meta": {}
}
```

See the full [Create Project action reference](actions/create-project.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/deskTime/latest/actions/create-project).
