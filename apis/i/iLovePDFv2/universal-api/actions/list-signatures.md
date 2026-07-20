# iLovePDFv2: List Signatures

Lists signature requests in iLovePDFv2.

```
GET https://connect.mindcloud.co/v1/universal/iLovePDFv2/latest/actions/list-signatures
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iLovePDFv2 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iLovePDFv2/latest/actions/list-signatures?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iLovePDFv2/latest/actions/list-signatures?${params}`, {
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
| `page` | number | no | Signature page, starting at 0. Default: `0`. |
| `perPage` | number | no | Number of signatures to return, from 1 to 100. Default: `20`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "expires": "2026-05-07T12:00:00.000Z",
      "files": [
        {}
      ],
      "name": "Ava Chen",
      "signers": [
        {}
      ],
      "status": "string",
      "token_requester": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `email` | string |  |
| `expires` | date |  |
| `files` | array<object> |  |
| `name` | string |  |
| `signers` | array<object> |  |
| `status` | string |  |
| `token_requester` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native iLovePDFv2 API, this operation is `GET /signature/list` (base URL `https://api.ilovepdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-signatures.md) for the provider-specific parameters and requirements.

