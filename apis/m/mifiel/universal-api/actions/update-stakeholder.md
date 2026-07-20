# Mifiel: Update Stakeholder

Updates a stakeholder for a document in Mifiel.

```
PUT https://connect.mindcloud.co/v1/universal/mifiel/latest/actions/update-stakeholder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mifiel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mifiel/latest/actions/update-stakeholder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentId": "string",
  "id": "string",
  "email": "ava@example.com",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mifiel/latest/actions/update-stakeholder', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentId": "string",
    "id": "string",
    "email": "ava@example.com",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentId` | string | yes | Document ID. |
| `id` | string | yes | Stakeholder ID. |
| `email` | string | yes | Stakeholder email address. |
| `name` | string | no | Stakeholder full name. |
| `taxId` | string | no | Tax ID (RFC in Mexico). |
| `sendInvite` | boolean | no | Whether to send invitation emails automatically. |
| `type` | string | yes | Type of stakeholder: signer or reviewer. |
| `allowedSignatureMethods[]` | array<string> | no | Allowed signature methods: FEA, FESCV, or FESSV. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "signed": true,
      "tax_id": "string",
      "type": "string",
      "widget_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Stakeholder email address |
| `id` | string | Unique identifier |
| `name` | string | Stakeholder full name |
| `signed` | boolean | Whether this person has signed |
| `tax_id` | string | Tax ID (RFC in Mexico) |
| `type` | string | Type of stakeholder |
| `widget_id` | string | Widget ID for signing interface |

## Native endpoint

Through the native Mifiel API, this operation is `PUT /api/v1/documents/:documentId/stakeholders/:id` (base URL `https://app.mifiel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-stakeholder.md) for the provider-specific parameters and requirements.

