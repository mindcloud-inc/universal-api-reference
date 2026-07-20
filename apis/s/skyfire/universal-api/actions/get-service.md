# Skyfire: Get Service

Retrieves a service from Skyfire.

```
GET https://connect.mindcloud.co/v1/universal/skyfire/latest/actions/get-service
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Skyfire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/skyfire/latest/actions/get-service?connectionId=$CONNECTION_ID&serviceId=41779894-ece2-4163-9761-b3b1b76e19b0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "serviceId": "41779894-ece2-4163-9761-b3b1b76e19b0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/skyfire/latest/actions/get-service?${params}`, {
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
| `serviceId` | string | yes | ID of the service to get. Example: `41779894-ece2-4163-9761-b3b1b76e19b0`. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acceptedTokens` | array<string> |  |
| `createdAt` | date |  |
| `description` | string |  |
| `humanIdentityRequirement` | object |  |
| `id` | string |  |
| `maxTokenTTLSeconds` | number |  |
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

Through the native Skyfire API, this operation is `GET /directory/services/:serviceId` (base URL `https://api.skyfire.xyz/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-service.md) for the provider-specific parameters and requirements.

