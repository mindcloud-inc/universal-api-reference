# Fixer: Get Historical Exchange Rates

Retrieves historical exchange rates from Fixer by date.

```
GET https://connect.mindcloud.co/v1/universal/fixer/latest/actions/get-historical-exchange-rates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fixer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fixer/latest/actions/get-historical-exchange-rates?connectionId=$CONNECTION_ID&date=YYYY-MM-DD" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "date": "YYYY-MM-DD"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fixer/latest/actions/get-historical-exchange-rates?${params}`, {
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
| `date` | string | yes | Historical date in YYYY-MM-DD format. Example: `YYYY-MM-DD`. |
| `symbols` | string | no | Optional comma-separated list of currency codes to limit the returned rates. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `base` | string | no | Optional three-letter base currency code. Fixer defaults to EUR and some plans restrict custom base currencies. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Three-letter ISO currency code. |
| `value` | number | Historical exchange rate for the requested code. |

## Native endpoint

Through the native Fixer API, this operation is `GET /:date` (base URL `https://data.fixer.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-historical-exchange-rates.md) for the provider-specific parameters and requirements.

