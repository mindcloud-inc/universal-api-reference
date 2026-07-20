# Extracta.ai Universal API Examples

These examples use the MindCloud API key and Extracta.ai connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Credits

Retrieves credits from Extracta.ai.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/extractaai/latest/actions/get-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/extractaai/latest/actions/get-credits?${params}`, {
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
      "credits": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Credits action reference](actions/get-credits.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/extractaai/latest/actions/get-credits).

## Create Classification

Creates a new classification in Extracta.ai.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/extractaai/latest/actions/create-classification" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "classificationDetails": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/extractaai/latest/actions/create-classification', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "classificationDetails": {}
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
      "classificationId": "string",
      "createdAt": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Classification action reference](actions/create-classification.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/extractaai/latest/actions/create-classification).
