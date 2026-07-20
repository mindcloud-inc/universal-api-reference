# ProductLift Universal API Examples

These examples use the MindCloud API key and ProductLift connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Portal



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productLift/latest/actions/get-portal?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productLift/latest/actions/get-portal?${params}`, {
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
      "editorType": "string",
      "guid": "string",
      "inviteMessage": "string",
      "jiraDomainUrl": "https://example.com",
      "jiraEnabled": true,
      "localization": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Portal action reference](actions/get-portal.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/productLift/latest/actions/get-portal).

## Add User To Group



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/productLift/latest/actions/add-user-to-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/productLift/latest/actions/add-user-to-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "group": "string",
      "success": true,
      "user": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add User To Group action reference](actions/add-user-to-group.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/productLift/latest/actions/add-user-to-group).
