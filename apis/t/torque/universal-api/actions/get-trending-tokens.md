# Torque: Get Trending Tokens



```
GET https://connect.mindcloud.co/v1/universal/torque/latest/actions/get-trending-tokens
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Torque `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/torque/latest/actions/get-trending-tokens?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/torque/latest/actions/get-trending-tokens?${params}`, {
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
| `chain` | string | no |  |
| `limit` | number | no | Maximum number of records to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chains": [
        {}
      ],
      "tokens": [
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
| `chains` | array<object> |  |
| `tokens` | array<object> |  |

## Native endpoint

Through the native Torque API, this operation is `GET /moralis/trending-tokens` (base URL `https://app.torque.fi/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-trending-tokens.md) for the provider-specific parameters and requirements.

