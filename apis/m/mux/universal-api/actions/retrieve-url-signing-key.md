# Mux: Retrieve URL Signing Key



```
GET https://connect.mindcloud.co/v1/universal/mux/latest/actions/retrieve-url-signing-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mux `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mux/latest/actions/retrieve-url-signing-key?connectionId=$CONNECTION_ID&signingKeyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "signingKeyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mux/latest/actions/retrieve-url-signing-key?${params}`, {
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
| `signingKeyId` | string | yes | The URL signing key ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |

## Native endpoint

Through the native Mux API, this operation is `GET /video/v1/signing-keys/{SIGNING_KEY_ID}` (base URL `https://api.mux.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-url-signing-key.md) for the provider-specific parameters and requirements.

