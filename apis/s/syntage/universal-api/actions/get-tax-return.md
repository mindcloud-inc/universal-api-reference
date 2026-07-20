# Syntage: Get Tax Return

Retrieves a tax return from Syntage.

```
GET https://connect.mindcloud.co/v1/universal/syntage/latest/actions/get-tax-return
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Syntage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/syntage/latest/actions/get-tax-return?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/syntage/latest/actions/get-tax-return?${params}`, {
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
| `id` | string | yes | The tax return identifier. |

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

Through the native Syntage API, this operation is `GET /tax-returns/:id` (base URL `https://api.sandbox.syntage.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tax-return.md) for the provider-specific parameters and requirements.

