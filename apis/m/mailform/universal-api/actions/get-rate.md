# Mailform: Get Rate



```
GET https://connect.mindcloud.co/v1/universal/mailform/latest/actions/get-rate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailform/latest/actions/get-rate?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com%2Fdocument.pdf&service=USPS_FIRST_CLASS&toName=Frank%20White&toAddress1=607%20North%20Avenue&toCity=Wakefield&toState=MA&toPostcode=01880&toCountry=US&fromName=Joe%20Green&fromAddress1=607%20North%20Avenue&fromCity=Wakefield&fromState=MA&fromPostcode=01880&fromCountry=US" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com/document.pdf",
  "service": "USPS_FIRST_CLASS",
  "toName": "Frank White",
  "toAddress1": "607 North Avenue",
  "toCity": "Wakefield",
  "toState": "MA",
  "toPostcode": "01880",
  "toCountry": "US",
  "fromName": "Joe Green",
  "fromAddress1": "607 North Avenue",
  "fromCity": "Wakefield",
  "fromState": "MA",
  "fromPostcode": "01880",
  "fromCountry": "US"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailform/latest/actions/get-rate?${params}`, {
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
| `url` | string | yes | URL of the PDF document to price. Example: `https://example.com/document.pdf`. |
| `customerReference` | string | no | Optional customer reference for the potential order. Example: `QUOTE-1001`. |
| `service` | list<string> | yes | Delivery service to price. One of: `0`, `1`, `10`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. Default: `USPS_FIRST_CLASS`. |
| `simplex` | boolean | no | Price one page per sheet when true; allow duplex when false. Default: `true`. |
| `color` | boolean | no | Price color printing when true; black and white when false. Default: `false`. |
| `toName` | string | yes | Name of the recipient. Example: `Frank White`. |
| `toAddress1` | string | yes | Street number and name of the recipient. Example: `607 North Avenue`. |
| `toCity` | string | yes | City of the recipient address. Example: `Wakefield`. |
| `toState` | string | yes | State of the recipient address. Example: `MA`. |
| `toPostcode` | string | yes | Postal or ZIP code of the recipient address. Example: `01880`. |
| `toCountry` | string | yes | Country of the recipient address. Example: `US`. |
| `fromName` | string | yes | Name of the sender. Example: `Joe Green`. |
| `fromAddress1` | string | yes | Street number and name of the sender. Example: `607 North Avenue`. |
| `fromCity` | string | yes | City of the sender address. Example: `Wakefield`. |
| `fromState` | string | yes | State of the sender address. Example: `MA`. |
| `fromPostcode` | string | yes | Postal or ZIP code of the sender address. Example: `01880`. |
| `fromCountry` | string | yes | Country of the sender address. Example: `US`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | no | PDF document to price. Use this or Url as the document source. |
| `webhook` | string | no | Webhook URL for order update notifications if the priced order is later created. Example: `https://example.com/mailform-webhook`. |
| `flat` | boolean | no | Price a flat envelope when true. |
| `stamp` | boolean | no | Price a real postage stamp when true. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pricing": {
        "cost": 1,
        "lineitems": [
          {
            "type": "string",
            "value": 1
          }
        ],
        "tax": 1,
        "total": 1
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pricing.cost` | number | Quoted order cost in the smallest currency unit. |
| `pricing.lineitems` | array<object> | Cost components that make up the quoted order price. |
| `pricing.lineitems[].type` | string | Cost component type. |
| `pricing.lineitems[].value` | number | Cost component amount in the smallest currency unit. |
| `pricing.tax` | number | Quoted tax in the smallest currency unit. |
| `pricing.total` | number | Quoted total in the smallest currency unit. |
| `success` | boolean | Whether Mailform generated the quote successfully. |

## Native endpoint

Through the native Mailform API, this operation is `POST /rates` (base URL `https://www.mailform.io/app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-rate.md) for the provider-specific parameters and requirements.

