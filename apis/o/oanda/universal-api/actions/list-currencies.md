# Oanda: List Currencies

Retrieves supported currency codes from Oanda.

```
GET https://connect.mindcloud.co/v1/universal/oanda/latest/actions/list-currencies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Oanda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oanda/latest/actions/list-currencies?connectionId=$CONNECTION_ID&ext=json" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ext": "json"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oanda/latest/actions/list-currencies?${params}`, {
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
| `data_set` | string | no | Dataset code to filter currencies. |
| `ext` | string | yes | Response format. Default: `json`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currencies": [
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
| `currencies` | array<object> | List of currencies returned by the dataset. |

## Native endpoint

Through the native Oanda API, this operation is `GET /v2/currencies.:ext` (base URL `https://exchange-rates-api.oanda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-currencies.md) for the provider-specific parameters and requirements.

