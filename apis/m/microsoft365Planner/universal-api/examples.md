# Microsoft 365 Planner Universal API Examples

These examples use the MindCloud API key and Microsoft 365 Planner connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get My Profile



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoft365Planner/latest/actions/get-my-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoft365Planner/latest/actions/get-my-profile?${params}`, {
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
      "businessPhones": [
        "string"
      ],
      "displayName": "Ava Chen",
      "givenName": "Ava Chen",
      "id": "string",
      "jobTitle": "string",
      "mail": "string",
      "mobilePhone": "string",
      "officeLocation": "string",
      "preferredLanguage": "string",
      "surname": "Ava Chen",
      "userPrincipalName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get My Profile action reference](actions/get-my-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/microsoft365Planner/latest/actions/get-my-profile).

## Create Bucket



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoft365Planner/latest/actions/create-bucket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Backlog",
  "planId": "xqQg5FS2LkCp935s-FIFm2QAFkHM"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoft365Planner/latest/actions/create-bucket', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Backlog",
    "planId": "xqQg5FS2LkCp935s-FIFm2QAFkHM"
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
      "id": "string",
      "name": "Ava Chen",
      "orderHint": "string",
      "planId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Bucket action reference](actions/create-bucket.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/microsoft365Planner/latest/actions/create-bucket).
