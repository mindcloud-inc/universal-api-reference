# Zoho Analytics Universal API Examples

These examples use the MindCloud API key and Zoho Analytics connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Organizations

Retrieves available organizations from Zoho Analytics.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/list-organizations?${params}`, {
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
      "data": {
        "orgs": [
          {
            "createdBy": "string",
            "createdByZuId": "string",
            "isDefault": true,
            "numberOfWorkspaces": 1,
            "orgDesc": "string",
            "orgId": "string",
            "orgName": "Ava Chen",
            "planName": "Ava Chen",
            "role": "string"
          }
        ]
      },
      "status": "string",
      "summary": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Organizations action reference](actions/list-organizations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoAnalytics/latest/actions/list-organizations).

## Add Row

Creates a row in a Zoho Analytics table.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/add-row" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "viewId": "string",
  "config": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/add-row', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
    "viewId": "string",
    "config": "[object Object]"
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
      "data": {
        "addedColumns": {},
        "invalidColumns": {}
      },
      "status": "string",
      "summary": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Row action reference](actions/add-row.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoAnalytics/latest/actions/add-row).
