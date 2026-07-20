# iLovePDFv2: Get Signature Status

Retrieves a signature request from iLovePDFv2 by requester token.

```
GET https://connect.mindcloud.co/v1/universal/iLovePDFv2/latest/actions/get-signature-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iLovePDFv2 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iLovePDFv2/latest/actions/get-signature-status?connectionId=$CONNECTION_ID&tokenRequester=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tokenRequester": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iLovePDFv2/latest/actions/get-signature-status?${params}`, {
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
| `tokenRequester` | string | yes | Signature requester token. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "name": "Ava Chen",
      "status": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `name` | string |  |
| `status` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native iLovePDFv2 API, this operation is `GET /signature/requesterview/:token_requester` (base URL `https://api.ilovepdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-signature-status.md) for the provider-specific parameters and requirements.

