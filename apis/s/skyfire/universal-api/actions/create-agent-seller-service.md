# Skyfire: Create Agent Seller Service

Creates a new agent seller service in Skyfire.

```
POST https://connect.mindcloud.co/v1/universal/skyfire/latest/actions/create-agent-seller-service
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Skyfire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/skyfire/latest/actions/create-agent-seller-service" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/skyfire/latest/actions/create-agent-seller-service', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Internal and public-facing service name. Example: `My API Service`. |
| `description` | string | no | What your service does and how buyers use it. Example: `Public description of the service`. |
| `serviceType` | string | no | Choose from API, Web Page, or MCP Server. Example: `API`. |
| `serviceUrl` | string | no | Provide the OpenAPI spec, public website URL, or MCP server endpoint depending on type. Example: `https://example.com/openapi.json`. |
| `price` | string | no | Price of the service in USD. Example: `0.01`. |
| `priceModel` | string | no | Per-use, per-MB, or subscription pricing model. Example: `PAY_PER_USE`. |
| `termsOfServiceUrl` | string | no | Link to your legal terms or usage policy. Example: `https://example.com/terms`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acceptedTokens": [
        "string"
      ],
      "active": true,
      "approved": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "humanIdentityRequirement": {},
      "id": "string",
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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acceptedTokens` | array<string> |  |
| `active` | boolean |  |
| `approved` | boolean |  |
| `createdAt` | date |  |
| `description` | string |  |
| `humanIdentityRequirement` | object |  |
| `id` | string |  |
| `minimumTokenAmount` | string |  |
| `name` | string |  |
| `openApiSpecUrl` | string |  |
| `price` | string |  |
| `priceModel` | string |  |
| `seller` | object |  |
| `tags` | array<string> |  |
| `termsOfService` | object |  |
| `type` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Skyfire API, this operation is `POST /agents/seller-services` (base URL `https://api.skyfire.xyz/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-agent-seller-service.md) for the provider-specific parameters and requirements.

