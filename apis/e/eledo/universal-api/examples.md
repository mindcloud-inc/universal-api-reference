# Eledo Universal API Examples

These examples use the MindCloud API key and Eledo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Profile

Retrieves the user's profile from Eledo.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eledo/latest/actions/get-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eledo/latest/actions/get-profile?${params}`, {
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
      "account": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Profile action reference](actions/get-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eledo/latest/actions/get-profile).

## Create File

Creates a new file in Eledo.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eledo/latest/actions/create-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eledo/latest/actions/create-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "string"
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
      "errors": [
        {}
      ],
      "filename": "Ava Chen",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create File action reference](actions/create-file.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eledo/latest/actions/create-file).
