# Hyperstack Certificates: Generate Credential Draft



```
POST https://connect.mindcloud.co/v1/universal/hyperstack/latest/actions/generate-credential-draft
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hyperstack Certificates `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hyperstack/latest/actions/generate-credential-draft" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "recipientName": "Ava Chen",
  "recipientEmail": "ava@example.com",
  "groupKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hyperstack/latest/actions/generate-credential-draft', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "recipientName": "Ava Chen",
    "recipientEmail": "ava@example.com",
    "groupKey": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `recipientName` | string | yes | Recipient full name for the draft credential. |
| `recipientEmail` | string | yes | Recipient email for the draft credential. |
| `groupKey` | string | yes | Credential group key used to generate the draft. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documentId": "string",
      "documentUrl": "https://example.com",
      "group": {},
      "issuedOn": "string",
      "metadata": {},
      "privacy": "string",
      "recipient": {},
      "status": "string",
      "success": true,
      "validUntil": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documentId` | string | Generated credential document identifier. |
| `documentUrl` | string | Public URL for the generated credential. |
| `group` | object | Credential group summary. |
| `issuedOn` | string | ISO timestamp when the draft credential was generated. |
| `metadata` | object | Additional credential metadata. |
| `privacy` | string | Credential visibility mode. |
| `recipient` | object | Recipient identity for the credential. |
| `status` | string | Credential lifecycle status. |
| `success` | boolean | Whether the draft credential was generated successfully. |
| `validUntil` | string | ISO timestamp when the credential expires, if any. |

## Native endpoint

Through the native Hyperstack Certificates API, this operation is `POST /credentials/generate` (base URL `https://api.thehyperstack.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-credential-draft.md) for the provider-specific parameters and requirements.

