# WhyDonate: Get Widget Donation Values



```
GET https://connect.mindcloud.co/v1/universal/whyDonate/latest/actions/get-widget-donation-values
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhyDonate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whyDonate/latest/actions/get-widget-donation-values?connectionId=$CONNECTION_ID&shortcode=wd-123456&currency=eur" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "shortcode": "wd-123456",
  "currency": "eur"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whyDonate/latest/actions/get-widget-donation-values?${params}`, {
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
| `shortcode` | string | yes | Widget shortcode used by the WordPress/widget donation values endpoint. Example: `wd-123456`. |
| `currency` | string | yes | Currency code selected in the widget before requesting donation values. Example: `eur`. |
| `mode` | string | no | Widget UI mode forwarded by the public script; the script falls back to form. Default: `form`. Example: `form`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currency": "string",
      "customdonationconfiguration": {
        "maxDonationAmount": "string",
        "minDonationAmount": "string",
        "monthly": {
          "default1": 1
        },
        "onetime": {
          "default1": 1
        }
      },
      "symbol": "string",
      "tipAmount": {
        "defaultValues": {
          "tipAmountFixedDefault": 1,
          "tipAmountPercentageDefault": 1
        }
      },
      "xToEur": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | string |  |
| `customdonationconfiguration.maxDonationAmount` | string |  |
| `customdonationconfiguration.minDonationAmount` | string |  |
| `customdonationconfiguration.monthly.default1` | number |  |
| `customdonationconfiguration.onetime.default1` | number |  |
| `symbol` | string |  |
| `tipAmount.defaultValues.tipAmountFixedDefault` | number |  |
| `tipAmount.defaultValues.tipAmountPercentageDefault` | number |  |
| `xToEur` | string |  |

## Native endpoint

Through the native WhyDonate API, this operation is `GET /fundraiser/wp/donation/values` (base URL `https://fundraiser.whydonate.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-widget-donation-values.md) for the provider-specific parameters and requirements.

