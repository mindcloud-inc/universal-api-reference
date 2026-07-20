# Skyfire: Get Token Charges

Retrieves token charges from Skyfire.

```
GET https://connect.mindcloud.co/v1/universal/skyfire/latest/actions/get-token-charges
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Skyfire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/skyfire/latest/actions/get-token-charges?connectionId=$CONNECTION_ID&tokenId=token-jti" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tokenId": "token-jti"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/skyfire/latest/actions/get-token-charges?${params}`, {
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
| `tokenId` | string | yes | The ID of the pay or kya-pay token. This is the value of the jti claim in the token body. Example: `token-jti`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "charges": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `charges` | array<object> |  |

## Native endpoint

Through the native Skyfire API, this operation is `GET /tokens/:tokenId/charges` (base URL `https://api.skyfire.xyz/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-token-charges.md) for the provider-specific parameters and requirements.

