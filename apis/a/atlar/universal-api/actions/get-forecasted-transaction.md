# Atlar: Get forecasted transaction

Retrieves a forecasted transaction from Atlar.

```
GET https://connect.mindcloud.co/v1/universal/atlar/latest/actions/get-forecasted-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atlar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/atlar/latest/actions/get-forecasted-transaction?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/atlar/latest/actions/get-forecasted-transaction?${params}`, {
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

Through the native Atlar API, this operation is `GET /analytics/v2beta/forecasted-transactions/{id}` (base URL `https://api.atlar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-forecasted-transaction.md) for the provider-specific parameters and requirements.

