# Atlar: Update loan

Updates an existing loan in Atlar.

```
PUT https://connect.mindcloud.co/v1/universal/atlar/latest/actions/update-loan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atlar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/atlar/latest/actions/update-loan" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/atlar/latest/actions/update-loan', {
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

Through the native Atlar API, this operation is `PATCH /financial-data/v2beta/loans/{id}` (base URL `https://api.atlar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-loan.md) for the provider-specific parameters and requirements.

