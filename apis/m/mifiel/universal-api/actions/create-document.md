# Mifiel: Create Document

Creates a new document in Mifiel.

```
POST https://connect.mindcloud.co/v1/universal/mifiel/latest/actions/create-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mifiel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mifiel/latest/actions/create-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string",
  "signatories[].email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mifiel/latest/actions/create-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string",
    "signatories[].email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | Document file in PDF format. |
| `signatories[]` | array<object> | no | List of signatories who will sign the document. |
| `signatories[].email` | string | yes | Signatory email address. |
| `signatories[].name` | string | no | Signatory full name. |
| `signatories[].taxId` | string | no | Signatory tax ID (RFC in Mexico). |
| `signatories[].allowedSignatureMethods[]` | array<string> | no | Allowed signature methods for the signatory: FEA, FESCV, or FESSV. |
| `daysToExpire` | number | no | Number of days before the document expires. |
| `externalId` | string | no | External ID for idempotency. |
| `sendInvites` | boolean | no | Whether to send invitation emails automatically. |
| `remindEvery` | number | no | How often to remind signers, in days. Supported values are 0, 1, 3, and 7. |
| `viewers[]` | array<object> | no | List of viewers who can access the document without signing. |
| `viewers[].email` | string | no | Viewer email address. |
| `viewers[].name` | string | no | Viewer full name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "original_hash": "string",
      "signed": true,
      "signers": [
        {}
      ],
      "state": "string",
      "viewers": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | Document creation timestamp |
| `id` | string | Unique identifier for the document |
| `original_hash` | string | SHA256 hash of the original document |
| `signed` | boolean | Whether the document has been signed by all parties |
| `signers` | array<object> | List of signatories for this document |
| `state` | string | Current status of the document |
| `viewers` | array<object> | List of viewers for this document |

## Native endpoint

Through the native Mifiel API, this operation is `POST /api/v1/documents` (base URL `https://app.mifiel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-document.md) for the provider-specific parameters and requirements.

