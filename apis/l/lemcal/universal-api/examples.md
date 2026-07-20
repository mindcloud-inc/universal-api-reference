# Lemcal Universal API Examples

These examples use the MindCloud API key and Lemcal connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Validate Authentication

Retrieves the authenticated user from Lemcal.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lemcal/latest/actions/validate-authentication?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lemcal/latest/actions/validate-authentication?${params}`, {
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
      "_id": "string",
      "createdAt": "string",
      "email": "ava@example.com",
      "publicIdentifier": "string"
    }
  ],
  "meta": {}
}
```

See the full [Validate Authentication action reference](actions/validate-authentication.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lemcal/latest/actions/validate-authentication).

## Create Hook

Creates a new hook in Lemcal.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lemcal/latest/actions/create-hook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "targetUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lemcal/latest/actions/create-hook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "targetUrl": "https://example.com"
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
      "_id": "string",
      "anyMeetingType": true,
      "createdAt": "string",
      "meetingTypeId": "string",
      "targetUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Hook action reference](actions/create-hook.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lemcal/latest/actions/create-hook).
