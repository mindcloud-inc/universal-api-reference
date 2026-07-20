# Atlar: Create entity

Creates an entity in Atlar.

```
POST https://connect.mindcloud.co/v1/universal/atlar/latest/actions/create-entity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atlar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/atlar/latest/actions/create-entity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "legalName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/atlar/latest/actions/create-entity', {
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
      "address": {},
      "created": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "legalName": "Ava Chen",
      "nationalIdentifier": {},
      "organizationId": "string",
      "parentId": "string",
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
| `address` | object |  |
| `created` | date |  |
| `id` | string |  |
| `legalName` | string |  |
| `nationalIdentifier` | object |  |
| `organizationId` | string |  |
| `parentId` | string |  |
| `updated` | date |  |
| `version` | number |  |

## Native endpoint

Through the native Atlar API, this operation is `POST /financial-data/v2/entities` (base URL `https://api.atlar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-entity.md) for the provider-specific parameters and requirements.

