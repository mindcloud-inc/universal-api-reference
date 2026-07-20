# Morningmate: Generate RSA Public Key

Retrieves an RSA public key from Morningmate.

```
GET https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/generate-rsa-public-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Morningmate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/generate-rsa-public-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/generate-rsa-public-key?${params}`, {
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
      "publicKey": "string",
      "userKey": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `publicKey` | string | RSA public key. |
| `userKey` | string | User identification key. |

## Native endpoint

Through the native Morningmate API, this operation is `GET /v1/sso` (base URL `https://api.morningmate.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-rsa-public-key.md) for the provider-specific parameters and requirements.

