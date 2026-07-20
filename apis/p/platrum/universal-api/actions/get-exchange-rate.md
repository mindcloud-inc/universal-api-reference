# Platrum: Get exchange rate

Retrieves a Platrum currency exchange rate by date.

```
GET https://connect.mindcloud.co/v1/universal/platrum/latest/actions/get-exchange-rate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Platrum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/platrum/latest/actions/get-exchange-rate?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/platrum/latest/actions/get-exchange-rate?${params}`, {
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
| `currency_code_from` | string | no | Source currency code. |
| `currency_code_to` | string | no | Target currency code. |
| `date` | date | no | Exchange-rate date. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Platrum API, this operation is `POST /finance/api/currency/exchange-rate` (base URL `https://3e8e7be.platrum.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-exchange-rate.md) for the provider-specific parameters and requirements.

