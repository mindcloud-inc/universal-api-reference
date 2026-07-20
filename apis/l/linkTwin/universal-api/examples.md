# LinkTwin Universal API Examples

These examples use the MindCloud API key and LinkTwin connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account

Retrieves your account details from LinkTwin.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/get-account?${params}`, {
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
      "currentPlan": "string",
      "email": "ava@example.com",
      "expired": "string",
      "expiryDate": {},
      "limits": {
        "alias": {
          "enabled": "string"
        },
        "clicks": 1,
        "delete": {
          "enabled": "string"
        },
        "domain": {
          "count": 1,
          "enabled": "string"
        },
        "export": {
          "enabled": "string"
        },
        "links": 1,
        "retention": 1,
        "team": {
          "count": 1,
          "enabled": "string"
        }
      },
      "settings": {
        "defaultDomain": "string",
        "timezone": "string",
        "timezoneOffset": 1
      },
      "usage": {
        "clicks": 1,
        "clicksResetDays": 1,
        "links": 1,
        "missedClicks": 1
      },
      "userId": 1,
      "verified": true
    }
  ],
  "meta": {}
}
```

See the full [Get Account action reference](actions/get-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/linkTwin/latest/actions/get-account).

## Assign Link To Collection

Assigns a link to a collection in LinkTwin.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/assign-link-to-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "collectionId": "string",
  "itemId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/assign-link-to-collection', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "collectionId": "string",
    "itemId": "string"
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
      "error": 1,
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Assign Link To Collection action reference](actions/assign-link-to-collection.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/linkTwin/latest/actions/assign-link-to-collection).
