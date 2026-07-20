# TravelPerk: Get Invoice PDF

Retrieves an invoice PDF from TravelPerk.

```
GET https://connect.mindcloud.co/v1/universal/travelPerk/latest/actions/get-invoice-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TravelPerk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/travelPerk/latest/actions/get-invoice-pdf?connectionId=$CONNECTION_ID&invoiceSerialNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "invoiceSerialNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/travelPerk/latest/actions/get-invoice-pdf?${params}`, {
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
| `invoiceSerialNumber` | string | yes | The invoice serial number whose PDF you want to download. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native TravelPerk API returns.

## Native endpoint

Through the native TravelPerk API, this operation is `GET /invoices/:invoiceSerialNumber/pdf` (base URL `https://api.sandbox-travelperk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invoice-pdf.md) for the provider-specific parameters and requirements.

