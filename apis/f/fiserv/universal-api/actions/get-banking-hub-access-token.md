# Fiserv: Get Banking Hub Access Token

Retrieves a Banking Hub access token from Fiserv.

```
GET https://connect.mindcloud.co/v1/universal/fiserv/latest/actions/get-banking-hub-access-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fiserv `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fiserv/latest/actions/get-banking-hub-access-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fiserv/latest/actions/get-banking-hub-access-token?${params}`, {
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
      "accessToken": "string",
      "expiresIn": "string",
      "tokenType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessToken` | string |  |
| `expiresIn` | string |  |
| `tokenType` | string |  |

## Native endpoint

Through the native Fiserv API, this operation is `POST https://bankinghub-cert.fiservapis.com/fts-apim/oauth2/v2` (base URL `https://bankinghub-cert.fiservapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-banking-hub-access-token.md) for the provider-specific parameters and requirements.

