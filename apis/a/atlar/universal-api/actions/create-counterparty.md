# Atlar: Create counterparty

Creates a counterparty in Atlar.

```
POST https://connect.mindcloud.co/v1/universal/atlar/latest/actions/create-counterparty
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atlar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/atlar/latest/actions/create-counterparty" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "legalName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/atlar/latest/actions/create-counterparty', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "legalName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `legalName` | string<string> | yes |  |

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

Through the native Atlar API, this operation is `POST /payments/v2/counterparties` (base URL `https://api.atlar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-counterparty.md) for the provider-specific parameters and requirements.

