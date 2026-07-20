# Intruder Universal API Examples

These examples use the MindCloud API key and Intruder connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check Health



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intruder/latest/actions/check-health?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intruder/latest/actions/check-health?${params}`, {
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
      "authenticatedAs": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Check Health action reference](actions/check-health.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/intruder/latest/actions/check-health).

## Add Target



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/intruder/latest/actions/add-target" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "address": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intruder/latest/actions/add-target', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "address": "string"
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
      "address": "string",
      "displayAddress": "string",
      "hasApiSchemas": true,
      "hasAuthentications": true,
      "id": 1,
      "licenseType": "string",
      "tags": [
        "string"
      ],
      "targetStatus": "string",
      "targetType": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Target action reference](actions/add-target.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/intruder/latest/actions/add-target).
