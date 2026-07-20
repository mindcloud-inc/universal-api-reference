# Presenton Universal API Examples

These examples use the MindCloud API key and Presenton connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Export Presentation



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/presenton/latest/actions/export-presentation?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/presenton/latest/actions/export-presentation?${params}`, {
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
      "creditsConsumed": 1,
      "editPath": "string",
      "path": "string",
      "presentationId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Export Presentation action reference](actions/export-presentation.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/presenton/latest/actions/export-presentation).

## Create Presentation From JSON



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/presenton/latest/actions/create-presentation-from-json" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "slides[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/presenton/latest/actions/create-presentation-from-json', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "slides[]": [{}]
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
      "creditsConsumed": 1,
      "editPath": "string",
      "path": "string",
      "presentationId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Presentation From JSON action reference](actions/create-presentation-from-json.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/presenton/latest/actions/create-presentation-from-json).
