# Atlar: Create loan

Creates a loan in Atlar.

```
POST https://connect.mindcloud.co/v1/universal/atlar/latest/actions/create-loan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atlar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/atlar/latest/actions/create-loan" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "string",
  "principalAmount": {},
  "terms": {},
  "lender": "string",
  "borrower": "string",
  "startDate": "2026-05-07T12:00:00.000Z",
  "timezone": "string",
  "amortizationType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/atlar/latest/actions/create-loan', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "string",
    "principalAmount": {},
    "terms": {},
    "lender": "string",
    "borrower": "string",
    "startDate": "2026-05-07T12:00:00.000Z",
    "timezone": "string",
    "amortizationType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string<string> | yes |  |
| `principalAmount` | object<string> | yes |  |
| `terms` | object<string> | yes |  |
| `lender` | string<string> | yes |  |
| `borrower` | string<string> | yes |  |
| `startDate` | date<string> | yes |  |
| `timezone` | string<string> | yes |  |
| `amortizationType` | string<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alias": "string",
      "amortizationSettlement": {},
      "amortizationType": "string",
      "borrower": "string",
      "closed": true,
      "created": "2026-05-07T12:00:00.000Z",
      "externalId": "string",
      "facilityId": "string",
      "id": "string",
      "interestSettlement": {},
      "lender": "string",
      "maturityDate": "2026-05-07T12:00:00.000Z",
      "organizationId": "string",
      "principalAmount": {},
      "recalculatingSince": "2026-05-07T12:00:00.000Z",
      "startDate": "2026-05-07T12:00:00.000Z",
      "terms": {},
      "timezone": "string",
      "type": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alias` | string |  |
| `amortizationSettlement` | object |  |
| `amortizationType` | string |  |
| `borrower` | string |  |
| `closed` | boolean |  |
| `created` | date |  |
| `externalId` | string |  |
| `facilityId` | string |  |
| `id` | string |  |
| `interestSettlement` | object |  |
| `lender` | string |  |
| `maturityDate` | date |  |
| `organizationId` | string |  |
| `principalAmount` | object |  |
| `recalculatingSince` | date |  |
| `startDate` | date |  |
| `terms` | object |  |
| `timezone` | string |  |
| `type` | string |  |
| `updated` | date |  |

## Native endpoint

Through the native Atlar API, this operation is `POST /financial-data/v2beta/loans` (base URL `https://api.atlar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-loan.md) for the provider-specific parameters and requirements.

