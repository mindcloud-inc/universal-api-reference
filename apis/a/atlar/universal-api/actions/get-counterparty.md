# Atlar: Get counterparty

Retrieves a counterparty from Atlar.

```
GET https://connect.mindcloud.co/v1/universal/atlar/latest/actions/get-counterparty
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atlar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/atlar/latest/actions/get-counterparty?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/atlar/latest/actions/get-counterparty?${params}`, {
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
| `id` | string<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accounts": [
        {}
      ],
      "address": {},
      "alias": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "entityIds": [
        {}
      ],
      "etag": "string",
      "externalId": "string",
      "id": "string",
      "legalName": "Ava Chen",
      "metadata": {},
      "nationalIdentifier": {},
      "organizationId": "string",
      "partyType": "string",
      "phone": "string",
      "updated": "2026-05-07T12:00:00.000Z",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accounts` | array<object> |  |
| `address` | object |  |
| `alias` | string |  |
| `created` | date |  |
| `email` | string |  |
| `entityIds` | array<object> |  |
| `etag` | string |  |
| `externalId` | string |  |
| `id` | string |  |
| `legalName` | string |  |
| `metadata` | object |  |
| `nationalIdentifier` | object |  |
| `organizationId` | string |  |
| `partyType` | string |  |
| `phone` | string |  |
| `updated` | date |  |
| `version` | number |  |

## Native endpoint

Through the native Atlar API, this operation is `GET /payments/v2/counterparties/{id}` (base URL `https://api.atlar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-counterparty.md) for the provider-specific parameters and requirements.

