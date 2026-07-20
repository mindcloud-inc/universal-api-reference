# Koncile OCR Universal API Examples

These examples use the MindCloud API key and Koncile OCR connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check API Key



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/check-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/check-api-key?${params}`, {
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
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Check API Key action reference](actions/check-api-key.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/koncileOCR/latest/actions/check-api-key).

## Create Field



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/create-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "format": "text",
  "name": "Ava Chen",
  "template_id": 1,
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/create-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "format": "text",
    "name": "Ava Chen",
    "template_id": 1,
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
      "desc": "string",
      "format": "string",
      "id": 1,
      "name": "Ava Chen",
      "position": 1,
      "template_id": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Field action reference](actions/create-field.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/koncileOCR/latest/actions/create-field).
