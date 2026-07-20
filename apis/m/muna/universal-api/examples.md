# Muna Universal API Examples

These examples use the MindCloud API key and Muna connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Retrieve Predictor

Retrieves a predictor from Muna by tag.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/muna/latest/actions/retrieve-predictor?connectionId=$CONNECTION_ID&tag=my-predictor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tag": "my-predictor"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/muna/latest/actions/retrieve-predictor?${params}`, {
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
      "access": "string",
      "card": "string",
      "description": "string",
      "name": "Ava Chen",
      "owner": {
        "created": "string",
        "username": "Ava Chen"
      },
      "signature": {
        "inputs": {
          "description": "string",
          "name": "Ava Chen",
          "optional": true,
          "type": "string"
        },
        "outputs": {
          "name": "Ava Chen",
          "type": "string"
        }
      },
      "status": "string",
      "tag": "string"
    }
  ],
  "meta": {}
}
```

See the full [Retrieve Predictor action reference](actions/retrieve-predictor.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/muna/latest/actions/retrieve-predictor).

## Create Prediction

Creates a prediction in Muna for a predictor tag.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/muna/latest/actions/create-prediction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tag": "my-predictor",
  "clientId": "client_123"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/muna/latest/actions/create-prediction', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tag": "my-predictor",
    "clientId": "client_123"
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
      "configuration": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "resources": {
        "name": "Ava Chen",
        "type": "string",
        "url": "https://example.com"
      },
      "tag": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Prediction action reference](actions/create-prediction.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/muna/latest/actions/create-prediction).
