# Supernotes: Find Card By Share Code

Retrieves a Supernotes card by share code.

```
GET https://connect.mindcloud.co/v1/universal/supernotes/latest/actions/find-card-by-share-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Supernotes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/supernotes/latest/actions/find-card-by-share-code?connectionId=$CONNECTION_ID&code=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "code": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/supernotes/latest/actions/find-card-by-share-code?${params}`, {
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
| `code` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "card": {},
      "cardId": "string",
      "code": "string",
      "grantedPerms": 1,
      "id": "string",
      "ownerId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `card` | object |  |
| `cardId` | string |  |
| `code` | string |  |
| `grantedPerms` | number |  |
| `id` | string |  |
| `ownerId` | string |  |

## Native endpoint

Through the native Supernotes API, this operation is `GET /sharing/code/:code` (base URL `https://api.supernotes.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-card-by-share-code.md) for the provider-specific parameters and requirements.

