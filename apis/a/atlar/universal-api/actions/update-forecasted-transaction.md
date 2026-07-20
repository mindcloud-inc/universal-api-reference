# Atlar: Update forecasted transaction

Updates an existing forecasted transaction in Atlar.

```
PUT https://connect.mindcloud.co/v1/universal/atlar/latest/actions/update-forecasted-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atlar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/atlar/latest/actions/update-forecasted-transaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/atlar/latest/actions/update-forecasted-transaction', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string<string> | yes |  |
| `If_Match` | string<string> | no |  |

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

Through the native Atlar API, this operation is `PATCH /analytics/v2beta/forecasted-transactions/{id}` (base URL `https://api.atlar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-forecasted-transaction.md) for the provider-specific parameters and requirements.

