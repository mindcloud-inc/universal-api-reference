# Stiply: Get Sign Request Signer

Retrieves a signer from a Stiply sign request.

```
GET https://connect.mindcloud.co/v1/universal/stiply/latest/actions/get-sign-request-signer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stiply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stiply/latest/actions/get-sign-request-signer?connectionId=$CONNECTION_ID&signRequest=1&signer=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "signRequest": "1",
  "signer": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stiply/latest/actions/get-sign-request-signer?${params}`, {
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
| `signRequest` | number | yes | Id of the signrequest. |
| `signer` | number | yes | Id of the signer. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachmentMessage": "string",
      "attachments": {
        "description": "string",
        "hasDocument": true,
        "id": 1,
        "optional": true
      },
      "authMethod": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "emandate": "string",
      "fields": {
        "document": 1,
        "height": 1,
        "optional": true,
        "page": 1,
        "signer": 1,
        "type": "string",
        "width": 1,
        "x": 1,
        "y": 1
      },
      "id": 1,
      "idin": "string",
      "key": "string",
      "language": "string",
      "name": "Ava Chen",
      "phone": "string",
      "redirectUrl": "https://example.com",
      "rejectReason": "string",
      "role": "string",
      "signerProgresses": {
        "action": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "ip": "string",
        "location": "string",
        "status": "string",
        "system": "string",
        "value": "string"
      },
      "signUrl": "https://example.com",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachmentMessage` | string |  |
| `attachments` | array<object> |  |
| `attachments.description` | string |  |
| `attachments.hasDocument` | boolean |  |
| `attachments.id` | number |  |
| `attachments.optional` | boolean |  |
| `authMethod` | string |  |
| `createdAt` | date |  |
| `email` | string |  |
| `emandate` | string |  |
| `fields` | array<object> |  |
| `fields.document` | number |  |
| `fields.height` | number |  |
| `fields.optional` | boolean |  |
| `fields.page` | number |  |
| `fields.signer` | number |  |
| `fields.type` | string |  |
| `fields.width` | number |  |
| `fields.x` | number |  |
| `fields.y` | number |  |
| `id` | number |  |
| `idin` | string |  |
| `key` | string |  |
| `language` | string |  |
| `name` | string |  |
| `phone` | string |  |
| `redirectUrl` | string |  |
| `rejectReason` | string |  |
| `role` | string |  |
| `signerProgresses` | array<object> |  |
| `signerProgresses.action` | string |  |
| `signerProgresses.createdAt` | date |  |
| `signerProgresses.ip` | string |  |
| `signerProgresses.location` | string |  |
| `signerProgresses.status` | string |  |
| `signerProgresses.system` | string |  |
| `signerProgresses.value` | string |  |
| `signUrl` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Stiply API, this operation is `GET /v2/sign_requests/:sign_request/signers/:signer` (base URL `https://api.stiply.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sign-request-signer.md) for the provider-specific parameters and requirements.

