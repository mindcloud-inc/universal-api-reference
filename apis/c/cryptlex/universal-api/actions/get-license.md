# Cryptlex: Get License

Retrieves a license from Cryptlex.

```
GET https://connect.mindcloud.co/v1/universal/cryptlex/latest/actions/get-license
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cryptlex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cryptlex/latest/actions/get-license?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cryptlex/latest/actions/get-license?${params}`, {
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
| `id` | string | yes | Unique identifier for the license. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowedActivations": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "key": "string",
      "productId": "string",
      "revoked": true,
      "suspended": true,
      "totalActivations": 1,
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userLocked": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowedActivations` | number |  |
| `createdAt` | date |  |
| `expiresAt` | date |  |
| `id` | string |  |
| `key` | string |  |
| `productId` | string |  |
| `revoked` | boolean |  |
| `suspended` | boolean |  |
| `totalActivations` | number |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `userLocked` | boolean |  |

## Native endpoint

Through the native Cryptlex API, this operation is `GET /v3/licenses/:id` (base URL `https://api.cryptlex.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-license.md) for the provider-specific parameters and requirements.

