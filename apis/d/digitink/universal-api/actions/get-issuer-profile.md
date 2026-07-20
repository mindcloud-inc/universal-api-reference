# Digit.ink: Get Issuer Profile



```
GET https://connect.mindcloud.co/v1/universal/digitink/latest/actions/get-issuer-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digit.ink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digitink/latest/actions/get-issuer-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digitink/latest/actions/get-issuer-profile?${params}`, {
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
      "@context": [
        "string"
      ],
      "description": "string",
      "email": "ava@example.com",
      "id": "string",
      "image": "string",
      "name": "Ava Chen",
      "publicKey": [
        {}
      ],
      "revocationList": "string",
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `@context` | array<string> |  |
| `description` | string |  |
| `email` | string |  |
| `id` | string |  |
| `image` | string |  |
| `name` | string |  |
| `publicKey` | array<object> |  |
| `revocationList` | string |  |
| `type` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Digit.ink API, this operation is `GET /issuers/:issuerPubkey` (base URL `https://app.digit.ink/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-issuer-profile.md) for the provider-specific parameters and requirements.

