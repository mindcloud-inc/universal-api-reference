# Billingo: Check Tax Number

Retrieves tax number validation details from Billingo.

```
GET https://connect.mindcloud.co/v1/universal/billingo/latest/actions/check-tax-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billingo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billingo/latest/actions/check-tax-number?connectionId=$CONNECTION_ID&taxNumber=12345678-1-42" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taxNumber": "12345678-1-42"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billingo/latest/actions/check-tax-number?${params}`, {
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
| `taxNumber` | string | yes | Tax number to validate. Default: `12332222-1-12`. Example: `12345678-1-42`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string",
      "tax_number": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string |  |
| `tax_number` | string |  |

## Native endpoint

Through the native Billingo API, this operation is `GET /utils/check-tax-number/:taxNumber` (base URL `https://api.billingo.hu/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-tax-number.md) for the provider-specific parameters and requirements.

