# Hyperstack Certificates: View Credential



```
GET https://connect.mindcloud.co/v1/universal/hyperstack/latest/actions/view-credential
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hyperstack Certificates `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hyperstack/latest/actions/view-credential?connectionId=$CONNECTION_ID&document_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "document_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hyperstack/latest/actions/view-credential?${params}`, {
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
| `document_id` | string | yes | The credential document identifier. |

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
| `documentId` | string | Credential document identifier. |
| `documentUrl` | string | Public URL for the credential. |
| `group` | object | Credential group summary. |
| `issuedOn` | string | ISO timestamp when the credential was issued. |
| `metadata` | object | Additional credential metadata. |
| `privacy` | string | Credential visibility mode. |
| `recipient` | object | Recipient identity for the credential. |
| `status` | string | Credential lifecycle status. |
| `success` | boolean | Whether the credential was loaded successfully. |
| `validUntil` | string | ISO timestamp when the credential expires, if any. |

## Native endpoint

Through the native Hyperstack Certificates API, this operation is `GET /credential/:document_id/view` (base URL `https://api.thehyperstack.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-credential.md) for the provider-specific parameters and requirements.

