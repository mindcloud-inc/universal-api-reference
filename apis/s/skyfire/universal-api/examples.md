# Skyfire Universal API Examples

These examples use the MindCloud API key and Skyfire connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Services

Retrieves services from Skyfire.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/skyfire/latest/actions/list-services?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/skyfire/latest/actions/list-services?${params}`, {
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
      "acceptedTokens": [
        "string"
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "humanIdentityRequirement": {},
      "id": "string",
      "maxTokenTTLSeconds": 1,
      "minimumTokenAmount": "string",
      "name": "Ava Chen",
      "openApiSpecUrl": "https://example.com",
      "price": "string",
      "priceModel": "string",
      "seller": {},
      "tags": [
        "string"
      ],
      "termsOfService": {},
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Services action reference](actions/list-services.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/skyfire/latest/actions/list-services).

## Activate Agent Seller Service

Activates an existing agent seller service in Skyfire.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/skyfire/latest/actions/activate-agent-seller-service" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sellerServiceId": "seller-service-id"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/skyfire/latest/actions/activate-agent-seller-service', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sellerServiceId": "seller-service-id"
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

See the full [Activate Agent Seller Service action reference](actions/activate-agent-seller-service.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/skyfire/latest/actions/activate-agent-seller-service).
