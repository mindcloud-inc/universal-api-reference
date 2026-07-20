# Atlar: Get facility

Retrieves a facility from Atlar.

```
GET https://connect.mindcloud.co/v1/universal/atlar/latest/actions/get-facility
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atlar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/atlar/latest/actions/get-facility?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/atlar/latest/actions/get-facility?${params}`, {
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
      "allowRollover": true,
      "borrowers": [
        {}
      ],
      "closed": true,
      "commitmentAmount": {},
      "created": "2026-05-07T12:00:00.000Z",
      "documents": [
        {}
      ],
      "drawdownAccountId": "string",
      "expiryDate": "2026-05-07T12:00:00.000Z",
      "externalId": "string",
      "feeSettlement": {},
      "feeTerms": {},
      "id": "string",
      "lender": "string",
      "organizationId": "string",
      "recalculatingSince": "2026-05-07T12:00:00.000Z",
      "terms": [
        {}
      ],
      "timezone": "string",
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
| `alias` | string |  |
| `allowRollover` | boolean |  |
| `borrowers` | array<object> |  |
| `closed` | boolean |  |
| `commitmentAmount` | object |  |
| `created` | date |  |
| `documents` | array<object> |  |
| `drawdownAccountId` | string |  |
| `expiryDate` | date |  |
| `externalId` | string |  |
| `feeSettlement` | object |  |
| `feeTerms` | object |  |
| `id` | string |  |
| `lender` | string |  |
| `organizationId` | string |  |
| `recalculatingSince` | date |  |
| `terms` | array<object> |  |
| `timezone` | string |  |
| `updated` | date |  |
| `version` | number |  |

## Native endpoint

Through the native Atlar API, this operation is `GET /financial-data/v2beta/facilities/{id}` (base URL `https://api.atlar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-facility.md) for the provider-specific parameters and requirements.

