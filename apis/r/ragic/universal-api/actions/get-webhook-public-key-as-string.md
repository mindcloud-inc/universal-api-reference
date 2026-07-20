# Ragic: Get Webhook Public Key As String

Retrieves the Ragic webhook public key as a string.

```
GET https://connect.mindcloud.co/v1/universal/ragic/latest/actions/get-webhook-public-key-as-string
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ragic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ragic/latest/actions/get-webhook-public-key-as-string?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ragic/latest/actions/get-webhook-public-key-as-string?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "publicKey": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | HTTP-like response code in the payload. |
| `publicKey` | string | Webhook public key as a base64-encoded string. |
| `status` | string | Ragic response status. |

## Native endpoint

Through the native Ragic API, this operation is `GET {{credentials.serverUrl}}/api/http/getWebhookSignaturePublicKey.jsp` (base URL `{{credentials.serverUrl}}/mindcloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook-public-key-as-string.md) for the provider-specific parameters and requirements.

