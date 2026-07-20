# Payfunnels: List Setup Fees

Retrieves a list of setup fees from Payfunnels.

```
GET https://connect.mindcloud.co/v1/universal/payfunnels/latest/actions/list-setup-fees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Payfunnels `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/payfunnels/latest/actions/list-setup-fees?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/payfunnels/latest/actions/list-setup-fees?${params}`, {
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
      "amount": 1,
      "currency": "string",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `currency` | string |  |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Payfunnels API, this operation is `GET /v1/fees/setup` (base URL `https://api.payfunnels.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-setup-fees.md) for the provider-specific parameters and requirements.

