# Poof: Fetch Price

Retrieves a price quote from Poof.

```
GET https://connect.mindcloud.co/v1/universal/poof/latest/actions/fetch-price
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Poof `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/poof/latest/actions/fetch-price?connectionId=$CONNECTION_ID&crypto=bitcoin" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "crypto": "bitcoin"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/poof/latest/actions/fetch-price?${params}`, {
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
| `crypto` | string | yes | Cryptocurrency or token symbol to price, for example bitcoin. Default: `bitcoin`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Poof API returns.

## Native endpoint

Through the native Poof API, this operation is `POST /price` (base URL `https://www.poof.io/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-price.md) for the provider-specific parameters and requirements.

