# Atlar: Create document

Creates a document in Atlar.

```
POST https://connect.mindcloud.co/v1/universal/atlar/latest/actions/create-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atlar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/atlar/latest/actions/create-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "glEntityId": "string",
  "type": "string",
  "amount": {},
  "date": "2026-05-07T12:00:00.000Z",
  "description": "string",
  "references": {},
  "voided": true,
  "reconciliationStatus": "string",
  "glEntries[]": [
    {}
  ],
  "provenance": {},
  "vendorCreated": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/atlar/latest/actions/create-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "glEntityId": "string",
    "type": "string",
    "amount": {},
    "date": "2026-05-07T12:00:00.000Z",
    "description": "string",
    "references": {},
    "voided": true,
    "reconciliationStatus": "string",
    "glEntries[]": [{}],
    "provenance": {},
    "vendorCreated": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `glEntityId` | string<string> | yes |  |
| `type` | string<string> | yes |  |
| `amount` | object<string> | yes |  |
| `date` | date<string> | yes |  |
| `description` | string<string> | yes |  |
| `references` | object<string> | yes |  |
| `voided` | boolean<string> | yes |  |
| `reconciliationStatus` | string<string> | yes |  |
| `glEntries[]` | array<object> | yes |  |
| `provenance` | object<string> | yes |  |
| `vendorCreated` | date<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": {},
      "appliedDocuments": [
        "string"
      ],
      "classification": "string",
      "counterparty": {},
      "date": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "glEntityId": "string",
      "glEntries": [
        "string"
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
| `appliedDocuments` | array |  |
| `classification` | string |  |
| `counterparty` | object |  |
| `date` | date |  |
| `description` | string |  |
| `glEntityId` | string |  |
| `glEntries` | array |  |
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

Through the native Atlar API, this operation is `POST /accounting/v2beta/documents` (base URL `https://api.atlar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-document.md) for the provider-specific parameters and requirements.

