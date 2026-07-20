# Atlar: Approve credit transfer

Approves a credit transfer in Atlar.

```
POST https://connect.mindcloud.co/v1/universal/atlar/latest/actions/approve-credit-transfer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atlar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/atlar/latest/actions/approve-credit-transfer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "approvalStepId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/atlar/latest/actions/approve-credit-transfer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "approvalStepId": "string"
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
| `approvalStepId` | string<string> | yes |  |

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
      "creatorUserId": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "destination": "string",
      "destinationHolder": {},
      "id": "string",
      "organizationId": "string",
      "reference": "string",
      "regulatoryReporting": [
        {}
      ],
      "scheme": "string",
      "schemeDetails": {},
      "source": {},
      "sourceHolder": {},
      "status": "string",
      "statusReason": {},
      "taxDetails": {}
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
| `creatorUserId` | string |  |
| `date` | date |  |
| `destination` | string |  |
| `destinationHolder` | object |  |
| `id` | string |  |
| `organizationId` | string |  |
| `reference` | string |  |
| `regulatoryReporting` | array<object> |  |
| `scheme` | string |  |
| `schemeDetails` | object |  |
| `source` | object |  |
| `sourceHolder` | object |  |
| `status` | string |  |
| `statusReason` | object |  |
| `taxDetails` | object |  |

## Native endpoint

Through the native Atlar API, this operation is `POST /payments/v2/credit-transfers/{id}:approve` (base URL `https://api.atlar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/approve-credit-transfer.md) for the provider-specific parameters and requirements.

