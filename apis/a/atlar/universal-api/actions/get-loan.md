# Atlar: Get loan

Retrieves a loan from Atlar.

```
GET https://connect.mindcloud.co/v1/universal/atlar/latest/actions/get-loan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atlar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/atlar/latest/actions/get-loan?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/atlar/latest/actions/get-loan?${params}`, {
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

Through the native Atlar API, this operation is `GET /financial-data/v2beta/loans/{id}` (base URL `https://api.atlar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-loan.md) for the provider-specific parameters and requirements.

