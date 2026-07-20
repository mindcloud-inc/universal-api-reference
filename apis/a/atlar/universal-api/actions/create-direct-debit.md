# Atlar: Create direct debit

Creates a direct debit in Atlar.

```
POST https://connect.mindcloud.co/v1/universal/atlar/latest/actions/create-direct-debit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atlar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/atlar/latest/actions/create-direct-debit" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "amount": "string",
  "scheme": "string",
  "date": "2026-05-07T12:00:00.000Z",
  "source": "string",
  "destination": {},
  "reference": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/atlar/latest/actions/create-direct-debit', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "amount": "string",
    "scheme": "string",
    "date": "2026-05-07T12:00:00.000Z",
    "source": "string",
    "destination": {},
    "reference": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `amount` | string<string> | yes |  |
| `scheme` | string<string> | yes |  |
| `date` | date<string> | yes |  |
| `source` | string<string> | yes |  |
| `destination` | object<string> | yes |  |
| `reference` | string<string> | yes |  |

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

Through the native Atlar API, this operation is `POST /payments/v2/direct-debits` (base URL `https://api.atlar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-direct-debit.md) for the provider-specific parameters and requirements.

