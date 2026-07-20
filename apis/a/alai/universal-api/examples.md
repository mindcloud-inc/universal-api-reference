# Alai Universal API Examples

These examples use the MindCloud API key and Alai connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Themes

Retrieves theme IDs and names from Alai.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alai/latest/actions/list-themes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alai/latest/actions/list-themes?${params}`, {
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
      "themes": [
        {
          "id": "string",
          "name": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Themes action reference](actions/list-themes.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/alai/latest/actions/list-themes).

## Create Slide

Creates an async slide generation in an Alai presentation.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/alai/latest/actions/create-slide" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "presentationId": "string",
  "slideContext": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/alai/latest/actions/create-slide', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "presentationId": "string",
    "slideContext": "string"
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
      "generationId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Slide action reference](actions/create-slide.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/alai/latest/actions/create-slide).
