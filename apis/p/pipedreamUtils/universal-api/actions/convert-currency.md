# Pipedream Utils: Helper Functions - Convert Currency

Converts an amount between currencies in Pipedream Utils.

```
GET https://connect.mindcloud.co/v1/universal/pipedreamUtils/latest/actions/convert-currency
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedream Utils `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipedreamUtils/latest/actions/convert-currency?connectionId=$CONNECTION_ID&fromCurrency=string&toCurrency=string&value=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fromCurrency": "string",
  "toCurrency": "string",
  "value": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipedreamUtils/latest/actions/convert-currency?${params}`, {
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
| `fromCurrency` | string | yes | The currency to convert from |
| `toCurrency` | string | yes | The currency to convert to |
| `value` | string | yes | The value to convert |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pipedream Utils API returns.

## Native endpoint

Through the native Pipedream Utils API, this operation is `GET` (base URL `https://pipedream.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-currency.md) for the provider-specific parameters and requirements.

