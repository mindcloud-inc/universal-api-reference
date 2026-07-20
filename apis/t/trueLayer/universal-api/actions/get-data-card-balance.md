# TrueLayer: Get Data Card Balance

Retrieves a data card balance from TrueLayer.

```
GET https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/get-data-card-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrueLayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/get-data-card-balance?connectionId=$CONNECTION_ID&card_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "card_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/get-data-card-balance?${params}`, {
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
| `card_id` | string | yes | TrueLayer Data API card ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account_id": "string",
      "available": 1,
      "currency": "string",
      "current": 1,
      "update_timestamp": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_id` | string |  |
| `available` | number |  |
| `currency` | string |  |
| `current` | number |  |
| `update_timestamp` | string |  |

## Native endpoint

Through the native TrueLayer API, this operation is `GET /data/v1/cards/:card_id/balance` (base URL `https://api.truelayer-sandbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-data-card-balance.md) for the provider-specific parameters and requirements.

