# BASIC: JSON Web Key Set

Retrieves the JSON Web Key Set from BASIC.

```
GET https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/j-son-web-key-set
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BASIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/j-son-web-key-set?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/j-son-web-key-set?${params}`, {
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
      "keys": [
        {
          "alg": "string",
          "e": "string",
          "kid": "string",
          "kty": "string",
          "n": "string",
          "use": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `keys[].alg` | string |  |
| `keys[].e` | string |  |
| `keys[].kid` | string |  |
| `keys[].kty` | string |  |
| `keys[].n` | string |  |
| `keys[].use` | string |  |

## Native endpoint

Through the native BASIC API, this operation is `GET /auth/.well-known/jwks.json` (base URL `https://api.basic.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/j-son-web-key-set.md) for the provider-specific parameters and requirements.

