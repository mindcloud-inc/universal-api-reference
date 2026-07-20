# Stiply: Get Sign Request

Retrieves a sign request from Stiply by ID.

```
GET https://connect.mindcloud.co/v1/universal/stiply/latest/actions/get-sign-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stiply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stiply/latest/actions/get-sign-request?connectionId=$CONNECTION_ID&signRequest=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "signRequest": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stiply/latest/actions/get-sign-request?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "allSignedAt": "string",
      "callBackUrl": "https://example.com",
      "canceledAt": "string",
      "comment": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "expiresAt": "string",
      "externalKey": "string",
      "id": 1,
      "key": "string",
      "message": "string",
      "rejectedAt": "string",
      "rejectReason": "string",
      "sentAt": "string",
      "signers": {
        "authMethod": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "email": "ava@example.com",
        "id": 1,
        "key": "string",
        "language": "string",
        "name": "Ava Chen",
        "phone": "string",
        "redirectUrl": "https://example.com",
        "role": "string",
        "signUrl": "https://example.com",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "signingSequenceType": "string",
      "signingType": "string",
      "status": "string",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "user": {
        "email": "ava@example.com",
        "id": 1,
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allSignedAt` | string |  |
| `callBackUrl` | string |  |
| `canceledAt` | string |  |
| `comment` | string |  |
| `createdAt` | date |  |
| `expiresAt` | string |  |
| `externalKey` | string |  |
| `id` | number |  |
| `key` | string |  |
| `message` | string |  |
| `rejectedAt` | string |  |
| `rejectReason` | string |  |
| `sentAt` | string |  |
| `signers` | array<object> |  |
| `signers.authMethod` | string |  |
| `signers.createdAt` | date |  |
| `signers.email` | string |  |
| `signers.id` | number |  |
| `signers.key` | string |  |
| `signers.language` | string |  |
| `signers.name` | string |  |
| `signers.phone` | string |  |
| `signers.redirectUrl` | string |  |
| `signers.role` | string |  |
| `signers.signUrl` | string |  |
| `signers.updatedAt` | date |  |
| `signingSequenceType` | string |  |
| `signingType` | string |  |
| `status` | string |  |
| `title` | string |  |
| `updatedAt` | date |  |
| `user` | object |  |
| `user.email` | string |  |
| `user.id` | number |  |
| `user.name` | string |  |

## Native endpoint

Through the native Stiply API, this operation is `GET /v2/sign_requests/:sign_request` (base URL `https://api.stiply.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sign-request.md) for the provider-specific parameters and requirements.

