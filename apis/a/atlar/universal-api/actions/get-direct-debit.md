# Atlar: Get direct debit

Retrieves a direct debit from Atlar.

```
GET https://connect.mindcloud.co/v1/universal/atlar/latest/actions/get-direct-debit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atlar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/atlar/latest/actions/get-direct-debit?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/atlar/latest/actions/get-direct-debit?${params}`, {
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
      "approvalSteps": [
        {}
      ],
      "attachedTransactions": [
        {}
      ],
      "categoryPurpose": "string",
      "chargeBearer": "string",
      "connectionInstructionId": "string",
      "creatorUserId": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "destination": {},
      "destinationHolder": {},
      "id": "string",
      "mandate": {},
      "organizationId": "string",
      "reference": "string",
      "scheme": "string",
      "schemeDetails": {},
      "source": {},
      "sourceHolder": {},
      "status": "string",
      "statusReason": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | object |  |
| `approvalSteps` | array<object> |  |
| `attachedTransactions` | array<object> |  |
| `categoryPurpose` | string |  |
| `chargeBearer` | string |  |
| `connectionInstructionId` | string |  |
| `creatorUserId` | string |  |
| `date` | date |  |
| `destination` | object |  |
| `destinationHolder` | object |  |
| `id` | string |  |
| `mandate` | object |  |
| `organizationId` | string |  |
| `reference` | string |  |
| `scheme` | string |  |
| `schemeDetails` | object |  |
| `source` | object |  |
| `sourceHolder` | object |  |
| `status` | string |  |
| `statusReason` | object |  |

## Native endpoint

Through the native Atlar API, this operation is `GET /payments/v2/direct-debits/{id}` (base URL `https://api.atlar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-direct-debit.md) for the provider-specific parameters and requirements.

