# Atlar: Update document

Updates an existing document in Atlar.

```
PUT https://connect.mindcloud.co/v1/universal/atlar/latest/actions/update-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atlar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/atlar/latest/actions/update-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/atlar/latest/actions/update-document', {
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
      "amount": {},
      "appliedDocuments": [
        {}
      ],
      "classification": "string",
      "counterparty": {},
      "date": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "glEntityId": "string",
      "glEntries": [
        {}
      ],
      "id": "string",
      "organizationId": "string",
      "provenance": {},
      "reconciliationMatchId": "string",
      "reconciliationStatus": "string",
      "reference": "string",
      "references": {},
      "remainingAmount": {},
      "type": "string",
      "vendorCreated": "2026-05-07T12:00:00.000Z",
      "vendorResourceUrl": "https://example.com",
      "voided": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | object |  |
| `appliedDocuments` | array<object> |  |
| `classification` | string |  |
| `counterparty` | object |  |
| `date` | date |  |
| `description` | string |  |
| `glEntityId` | string |  |
| `glEntries` | array<object> |  |
| `id` | string |  |
| `organizationId` | string |  |
| `provenance` | object |  |
| `reconciliationMatchId` | string |  |
| `reconciliationStatus` | string |  |
| `reference` | string |  |
| `references` | object |  |
| `remainingAmount` | object |  |
| `type` | string |  |
| `vendorCreated` | date |  |
| `vendorResourceUrl` | string |  |
| `voided` | boolean |  |

## Native endpoint

Through the native Atlar API, this operation is `PATCH /accounting/v2beta/documents/{id}` (base URL `https://api.atlar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-document.md) for the provider-specific parameters and requirements.

