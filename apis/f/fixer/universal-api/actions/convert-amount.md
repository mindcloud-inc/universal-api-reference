# Fixer: Convert Amount

Converts an amount between currencies in Fixer.

```
GET https://connect.mindcloud.co/v1/universal/fixer/latest/actions/convert-amount
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fixer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fixer/latest/actions/convert-amount?connectionId=$CONNECTION_ID&from=string&to=string&amount=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "from": "string",
  "to": "string",
  "amount": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fixer/latest/actions/convert-amount?${params}`, {
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
| `from` | string | yes | Three-letter currency code to convert from. |
| `to` | string | yes | Three-letter currency code to convert to. |
| `amount` | number | yes | Amount to convert. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `date` | string | no | Optional historical date in YYYY-MM-DD format for historical conversion. Example: `YYYY-MM-DD`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "date": "string",
      "from": "string",
      "historical": true,
      "rate": 1,
      "result": 1,
      "to": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number | Original amount before conversion. |
| `date` | string | Effective conversion date in YYYY-MM-DD format. |
| `from` | string | Source currency code. |
| `historical` | boolean | Whether the conversion used a historical date. |
| `rate` | number | Applied conversion rate. |
| `result` | number | Converted amount. |
| `to` | string | Target currency code. |

## Native endpoint

Through the native Fixer API, this operation is `GET /convert` (base URL `https://data.fixer.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-amount.md) for the provider-specific parameters and requirements.

