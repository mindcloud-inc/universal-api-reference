# Abyssale Universal API Examples

These examples use the MindCloud API key and Abyssale connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Fonts

Retrieves available fonts from Abyssale.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/abyssale/latest/actions/get-fonts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/abyssale/latest/actions/get-fonts?${params}`, {
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
      "availableWeights": [
        1
      ],
      "id": "string",
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Fonts action reference](actions/get-fonts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/abyssale/latest/actions/get-fonts).

## Create Banner Export ZIP

Exports Abyssale banners as a ZIP archive.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/abyssale/latest/actions/create-banner-export-zip" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ids[]": [
    "string"
  ],
  "callback_url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/abyssale/latest/actions/create-banner-export-zip', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ids[]": ["string"],
    "callback_url": "https://example.com"
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

See the full [Create Banner Export ZIP action reference](actions/create-banner-export-zip.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/abyssale/latest/actions/create-banner-export-zip).
