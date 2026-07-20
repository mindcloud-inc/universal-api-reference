# Rye: List Checkout Intents

Retrieves checkout intents from Rye.

```
GET https://connect.mindcloud.co/v1/universal/rye/latest/actions/list-checkout-intents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rye `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rye/latest/actions/list-checkout-intents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rye/latest/actions/list-checkout-intents?${params}`, {
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
| `id[]` | array<string> | no | Filter by checkout intent ids. Accepts multiple values as an array. |
| `state[]` | array<string> | no | Filter by checkout intent states. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "pageInfo": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `pageInfo` | object |  |

## Native endpoint

Through the native Rye API, this operation is `GET /api/v1/checkout-intents` (base URL `https://staging.api.rye.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-checkout-intents.md) for the provider-specific parameters and requirements.

