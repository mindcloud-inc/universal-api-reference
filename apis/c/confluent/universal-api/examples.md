# Confluent Universal API Examples

These examples use the MindCloud API key and Confluent connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Organizations

Retrieves organizations from your Confluent Cloud account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/confluent/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/confluent/latest/actions/list-organizations?${params}`, {
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
      "apiVersion": "string",
      "data": [
        {
          "displayName": "Ava Chen",
          "id": "string",
          "jitEnabled": true
        }
      ],
      "kind": "string",
      "metadata": {}
    }
  ],
  "meta": {}
}
```

See the full [List Organizations action reference](actions/list-organizations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/confluent/latest/actions/list-organizations).

## Create API Key

Creates a new API key in Confluent Cloud.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/confluent/latest/actions/create-api-key" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "spec.owner.id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/confluent/latest/actions/create-api-key', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "spec.owner.id": "string"
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
      "apiVersion": "string",
      "id": "string",
      "kind": "string",
      "metadata": {},
      "spec": {}
    }
  ],
  "meta": {}
}
```

See the full [Create API Key action reference](actions/create-api-key.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/confluent/latest/actions/create-api-key).
