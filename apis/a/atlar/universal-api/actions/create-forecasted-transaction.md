# Atlar: Create forecasted transaction

Creates a forecasted transaction in Atlar.

```
POST https://connect.mindcloud.co/v1/universal/atlar/latest/actions/create-forecasted-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atlar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/atlar/latest/actions/create-forecasted-transaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "parent": "string",
  "description": "string",
  "amount": "string",
  "date": "2026-05-07T12:00:00.000Z",
  "origin": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/atlar/latest/actions/create-forecasted-transaction', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "parent": "string",
    "description": "string",
    "amount": "string",
    "date": "2026-05-07T12:00:00.000Z",
    "origin": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `parent` | string<string> | yes |  |
| `description` | string<string> | yes |  |
| `amount` | string<string> | yes |  |
| `date` | date<string> | yes |  |
| `origin` | object<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": {},
      "counterparty": {},
      "created": "2026-05-07T12:00:00.000Z",
      "date": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "etag": "string",
      "externalId": "string",
      "id": "string",
      "metadata": {},
      "organizationId": "string",
      "origin": {},
      "parent": "string",
      "scenarioId": "string",
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
| `amount` | object |  |
| `counterparty` | object |  |
| `created` | date |  |
| `date` | date |  |
| `description` | string |  |
| `etag` | string |  |
| `externalId` | string |  |
| `id` | string |  |
| `metadata` | object |  |
| `organizationId` | string |  |
| `origin` | object |  |
| `parent` | string |  |
| `scenarioId` | string |  |
| `updated` | date |  |
| `version` | number |  |

## Native endpoint

Through the native Atlar API, this operation is `POST /analytics/v2beta/forecasted-transactions` (base URL `https://api.atlar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-forecasted-transaction.md) for the provider-specific parameters and requirements.

