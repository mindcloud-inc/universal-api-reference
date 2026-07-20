# Aspose Universal API Examples

These examples use the MindCloud API key and Aspose connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get API Information

Retrieves Slides API information from Aspose.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspose/latest/actions/get-api-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspose/latest/actions/get-api-information?${params}`, {
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

See the full [Get API Information action reference](actions/get-api-information.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/aspose/latest/actions/get-api-information).

## Add Custom Properties

Creates custom document properties in Aspose.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aspose/latest/actions/add-custom-properties" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "properties": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aspose/latest/actions/add-custom-properties', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "properties": {}
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

See the full [Add Custom Properties action reference](actions/add-custom-properties.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/aspose/latest/actions/add-custom-properties).
