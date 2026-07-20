# Common Ninja Universal API Examples

These examples use the MindCloud API key and Common Ninja connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User Details

Retrieves user details from Common Ninja.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/commonNinja/latest/actions/get-user-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/commonNinja/latest/actions/get-user-details?${params}`, {
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
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get User Details action reference](actions/get-user-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/commonNinja/latest/actions/get-user-details).

## Create Widget

Creates a widget in Common Ninja.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/commonNinja/latest/actions/create-widget" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "status": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/commonNinja/latest/actions/create-widget', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "status": "string",
    "type": "string"
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
      "created": "2026-05-07T12:00:00.000Z",
      "data": {},
      "description": "string",
      "editorUrl": "https://example.com",
      "embedCode": {},
      "id": "string",
      "modelVersion": 1,
      "name": "Ava Chen",
      "previewImage": "string",
      "projectId": "string",
      "slug": "string",
      "status": "string",
      "type": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Create Widget action reference](actions/create-widget.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/commonNinja/latest/actions/create-widget).
