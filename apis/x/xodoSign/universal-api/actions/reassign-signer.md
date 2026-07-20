# Xodo Sign: Reassign Signer

Reassigns a document signer to another person in Xodo Sign.

```
PUT https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/reassign-signer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xodo Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/reassign-signer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "business_id": "string",
  "document_hash": "string",
  "signer_id": "string",
  "new_signer_name": "Ava Chen",
  "new_signer_email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/reassign-signer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "business_id": "string",
    "document_hash": "string",
    "signer_id": "string",
    "new_signer_name": "Ava Chen",
    "new_signer_email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `business_id` | string | yes | Business ID to scope the reassignment request. |
| `document_hash` | string | yes | Unique document hash whose signer should be reassigned. |
| `signer_id` | string | yes | Signer ID that should be replaced. |
| `new_signer_name` | string | yes | Display name of the replacement signer. |
| `new_signer_email` | string | yes | Email address of the replacement signer. |
| `reason` | string | no | Optional reason for the reassignment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the signer reassignment request succeeded. |

## Native endpoint

Through the native Xodo Sign API, this operation is `POST /reassign` (base URL `https://api.eversign.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reassign-signer.md) for the provider-specific parameters and requirements.

