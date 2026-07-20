# iLovePDFv2: Get Receiver Info

Retrieves a signature receiver from iLovePDFv2 by receiver token.

```
GET https://connect.mindcloud.co/v1/universal/iLovePDFv2/latest/actions/get-receiver-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iLovePDFv2 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iLovePDFv2/latest/actions/get-receiver-info?connectionId=$CONNECTION_ID&receiverTokenRequester=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "receiverTokenRequester": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iLovePDFv2/latest/actions/get-receiver-info?${params}`, {
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
| `receiverTokenRequester` | string | yes | Receiver token requester value. |

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

Through the native iLovePDFv2 API, this operation is `GET /signature/receiver/info/:receiver_token_requester` (base URL `https://api.ilovepdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-receiver-info.md) for the provider-specific parameters and requirements.

