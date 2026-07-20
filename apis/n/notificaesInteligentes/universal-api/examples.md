# Notificações Inteligentes Universal API Examples

These examples use the MindCloud API key and Notificações Inteligentes connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Integrations

Retrieves integrations from Notificações Inteligentes.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/notificaesInteligentes/latest/actions/list-integrations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/notificaesInteligentes/latest/actions/list-integrations?${params}`, {
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
      "data": [
        {}
      ],
      "links": {},
      "meta": {}
    }
  ],
  "meta": {}
}
```

See the full [List Integrations action reference](actions/list-integrations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/notificaesInteligentes/latest/actions/list-integrations).

## Create Integration

Creates a new integration in Notificações Inteligentes.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/notificaesInteligentes/latest/actions/create-integration" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "platform": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/notificaesInteligentes/latest/actions/create-integration', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "platform": "string"
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
      "data": {}
    }
  ],
  "meta": {}
}
```

See the full [Create Integration action reference](actions/create-integration.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/notificaesInteligentes/latest/actions/create-integration).
