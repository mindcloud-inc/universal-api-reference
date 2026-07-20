# Skyfire: Get Agent Seller Service

Retrieves an agent seller service from Skyfire.

```
GET https://connect.mindcloud.co/v1/universal/skyfire/latest/actions/get-agent-seller-service
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Skyfire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/skyfire/latest/actions/get-agent-seller-service?connectionId=$CONNECTION_ID&sellerServiceId=seller-service-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sellerServiceId": "seller-service-id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/skyfire/latest/actions/get-agent-seller-service?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sellerServiceId` | string | yes | The ID of the seller service to get. Example: `seller-service-id`. |

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

Through the native Skyfire API, this operation is `GET /agents/seller-services/:sellerServiceId` (base URL `https://api.skyfire.xyz/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-agent-seller-service.md) for the provider-specific parameters and requirements.

