# PromptHub Universal API Examples

These examples use the MindCloud API key and PromptHub connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Authenticated User

Retrieves the authenticated user from PromptHub.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/promptHub/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/promptHub/latest/actions/get-authenticated-user?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Get Authenticated User action reference](actions/get-authenticated-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/promptHub/latest/actions/get-authenticated-user).

## Run Project

Runs a PromptHub project by project ID.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/promptHub/latest/actions/run-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/promptHub/latest/actions/run-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Run Project action reference](actions/run-project.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/promptHub/latest/actions/run-project).
