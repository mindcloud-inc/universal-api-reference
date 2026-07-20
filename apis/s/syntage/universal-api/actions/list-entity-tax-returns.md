# Syntage: List Entity Tax Returns

Retrieves tax returns for an entity in Syntage.

```
GET https://connect.mindcloud.co/v1/universal/syntage/latest/actions/list-entity-tax-returns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Syntage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/syntage/latest/actions/list-entity-tax-returns?connectionId=$CONNECTION_ID&entityId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "entityId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/syntage/latest/actions/list-entity-tax-returns?${params}`, {
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
| `entityId` | string | yes | The Syntage entity identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "@id": "string",
      "@type": "string",
      "captureLine": "string",
      "complementary": "string",
      "createdAt": "string",
      "files": [
        {}
      ],
      "fiscalYear": "string",
      "id": "string",
      "intervalUnit": "string",
      "operationNumber": 1,
      "payment": {},
      "period": "string",
      "presentedAt": "2026-05-07T12:00:00.000Z",
      "taxpayer": {},
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `@id` | string |  |
| `@type` | string |  |
| `captureLine` | string |  |
| `complementary` | string |  |
| `createdAt` | string |  |
| `files` | array<object> |  |
| `fiscalYear` | string |  |
| `id` | string |  |
| `intervalUnit` | string |  |
| `operationNumber` | number |  |
| `payment` | object |  |
| `period` | string |  |
| `presentedAt` | date |  |
| `taxpayer` | object |  |
| `type` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Syntage API, this operation is `GET /entities/:entityId/tax-returns` (base URL `https://api.sandbox.syntage.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-entity-tax-returns.md) for the provider-specific parameters and requirements.

