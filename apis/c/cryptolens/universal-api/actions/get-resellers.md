# Cryptolens: Get Resellers

Retrieves resellers from Cryptolens.

```
GET https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/get-resellers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cryptolens `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/get-resellers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/get-resellers?${params}`, {
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
      "created": "string",
      "description": "string",
      "email": "ava@example.com",
      "id": 1,
      "inviteId": 1,
      "metadata": {},
      "name": "Ava Chen",
      "phone": "string",
      "resellerUserId": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | string | Get Resellers response field `created` from Cryptolens docs example. |
| `description` | string | Get Resellers response field `description` from Cryptolens docs example. |
| `email` | string | Get Resellers response field `email` from Cryptolens docs example. |
| `id` | number | Get Resellers response field `id` from Cryptolens docs example. |
| `inviteId` | number | Get Resellers response field `inviteId` from Cryptolens docs example. |
| `metadata` | object | Get Resellers response field `metadata` from Cryptolens docs example. |
| `name` | string | Get Resellers response field `name` from Cryptolens docs example. |
| `phone` | string | Get Resellers response field `phone` from Cryptolens docs example. |
| `resellerUserId` | number | Get Resellers response field `resellerUserId` from Cryptolens docs example. |
| `url` | string | Get Resellers response field `url` from Cryptolens docs example. |

## Native endpoint

Through the native Cryptolens API, this operation is `GET /api/reseller/GetResellers` (base URL `https://api.cryptolens.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-resellers.md) for the provider-specific parameters and requirements.

