# SMS.to: Monthly Usage Report

Retrieves a monthly usage report from SMS.to.

```
GET https://connect.mindcloud.co/v1/universal/sMSto/latest/actions/monthly-usage-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMS.to `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSto/latest/actions/monthly-usage-report?connectionId=$CONNECTION_ID&billingMonth=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "billingMonth": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSto/latest/actions/monthly-usage-report?${params}`, {
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
| `billingMonth` | string | yes | Billing month to report on. Format: YYYY-MM. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `product` | list<string> | no | Product to report usage for. Possible values: MESSAGING, VERIFY. One of: `MESSAGING`, `VERIFY`. |
| `channel[]` | array<string> | no | Channels to include in the report. Possible values: SMS, VIBER, WHATSAPP, TELEGRAM. |
| `country[]` | array<string> | no | Destination country codes (ISO-3166-1 alpha-2). |
| `network` | boolean | no | Filter by network. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billingCurrency": "string",
      "results": [
        {
          "channel": "string",
          "chargedPrice": 1,
          "chargedPriceEur": 1,
          "country": "string",
          "mccMnc": 1,
          "month": "string",
          "network": "string",
          "product": "string",
          "quantity": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingCurrency` | string |  |
| `results[].channel` | string |  |
| `results[].chargedPrice` | number |  |
| `results[].chargedPriceEur` | number |  |
| `results[].country` | string |  |
| `results[].mccMnc` | number |  |
| `results[].month` | string |  |
| `results[].network` | string |  |
| `results[].product` | string |  |
| `results[].quantity` | number |  |

## Native endpoint

Through the native SMS.to API, this operation is `POST /v1/reports/monthly-usage` (base URL `https://api.sms.to`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/monthly-usage-report.md) for the provider-specific parameters and requirements.

