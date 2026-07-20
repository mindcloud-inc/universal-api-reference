# Mailform: Create Order



```
POST https://connect.mindcloud.co/v1/universal/mailform/latest/actions/create-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailform/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
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
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailform/latest/actions/create-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
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
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | no | URL of the PDF document to mail. Ignored if File is provided. Example: `https://example.com/document.pdf`. |
| `customerReference` | string | no | Optional customer reference to attach to the order. Example: `ORDER-1001`. |
| `service` | list<string> | yes | Delivery service to use for the order. One of: `0`, `1`, `10`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. Default: `USPS_FIRST_CLASS`. |
| `simplex` | boolean | no | Print one page per sheet when true; allow duplex when false. Default: `true`. |
| `color` | boolean | no | Print in color when true; black and white when false. Default: `false`. |
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
| `file` | file | no | PDF document to mail. Use this, Url, or Template as the document source. |
| `template` | string | no | Mailform template identifier to use as the document source. |
| `variables` | object | no | JSON object of template variables. Used only when Template is provided. |
| `webhook` | string | no | Webhook URL for order update notifications. Example: `https://example.com/mailform-webhook`. |
| `company` | string | no | Company ID to associate with the order. |
| `flat` | boolean | no | Require mailing in a flat envelope when true. |
| `stamp` | boolean | no | Require a real postage stamp when true. |
| `returnEnvelope` | boolean | no | Include a return envelope when true. |
| `message` | string | no | Message for postcard or notecard services. |
| `qrcode` | string | no | QR code to print on supported USPS postcard and first-class mail. |
| `toOrganization` | string | no | Organization or company associated with the recipient. |
| `toAddress2` | string | no | Suite, room, or secondary address for the recipient. Example: `Door 18`. |
| `fromOrganization` | string | no | Organization or company associated with the sender. |
| `fromAddress2` | string | no | Suite, room, or secondary address for the sender. Example: `Door 18`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Mailform API returns.

## Native endpoint

Through the native Mailform API, this operation is `POST /orders` (base URL `https://www.mailform.io/app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order.md) for the provider-specific parameters and requirements.

