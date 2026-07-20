# TrueLayer: Get Merchant Account

Retrieves a merchant account from TrueLayer.

```
GET https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/get-merchant-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrueLayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/get-merchant-account?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/get-merchant-account?${params}`, {
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
| `id` | string | yes | TrueLayer merchant account ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account_identifiers": [
        {}
      ],
      "available_balance": 1,
      "currency": "string",
      "current_balance": 1,
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
| `account_identifiers` | array<object> |  |
| `available_balance` | number |  |
| `currency` | string |  |
| `current_balance` | number |  |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native TrueLayer API, this operation is `GET /v3/merchant-accounts/:id` (base URL `https://api.truelayer-sandbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-merchant-account.md) for the provider-specific parameters and requirements.

