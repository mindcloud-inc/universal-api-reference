# Stiply: List Sign Request Signers

Retrieves signers for a Stiply sign request.

```
GET https://connect.mindcloud.co/v1/universal/stiply/latest/actions/list-sign-request-signers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stiply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stiply/latest/actions/list-sign-request-signers?connectionId=$CONNECTION_ID&signRequest=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "signRequest": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stiply/latest/actions/list-sign-request-signers?${params}`, {
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
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authMethod` | string |  |
| `createdAt` | date |  |
| `email` | string |  |
| `id` | number |  |
| `key` | string |  |
| `language` | string |  |
| `name` | string |  |
| `phone` | string |  |
| `redirectUrl` | string |  |
| `role` | string |  |
| `signUrl` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Stiply API, this operation is `GET /v2/sign_requests/:sign_request/signers` (base URL `https://api.stiply.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sign-request-signers.md) for the provider-specific parameters and requirements.

