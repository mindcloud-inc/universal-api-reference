# Oboloo: Create Contract Document Type

Creates a new contract document type in Oboloo.

```
POST https://connect.mindcloud.co/v1/universal/oboloo/latest/actions/create-contract-document-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Oboloo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oboloo/latest/actions/create-contract-document-type" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contract_document_type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oboloo/latest/actions/create-contract-document-type', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contract_document_type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contract_document_type` | string | yes | Title of the contract document type to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documentType": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "createdBy": 1,
        "createdType": "string",
        "id": 1,
        "name": "Ava Chen",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documentType.createdAt` | date |  |
| `documentType.createdBy` | number |  |
| `documentType.createdType` | string |  |
| `documentType.id` | number |  |
| `documentType.name` | string |  |
| `documentType.updatedAt` | date |  |
| `message` | string |  |

## Native endpoint

Through the native Oboloo API, this operation is `POST /configuration/add-contract-document-Types` (base URL `https://mindcloudwizard20260330.oboloo.app/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contract-document-type.md) for the provider-specific parameters and requirements.

