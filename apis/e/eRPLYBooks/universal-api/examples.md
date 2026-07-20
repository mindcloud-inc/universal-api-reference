# ERPLY Books Universal API Examples

These examples use the MindCloud API key and ERPLY Books connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Company Info

Retrieves company information from ERPLY Books.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eRPLYBooks/latest/actions/get-company-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eRPLYBooks/latest/actions/get-company-info?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "records": [
        {
          "address": "string",
          "address2": "string",
          "bankAccountNumber": "string",
          "bankAccountNumber2": "string",
          "bankIBAN": "string",
          "bankIBAN2": "string",
          "bankName": "Ava Chen",
          "bankName2": "Ava Chen",
          "bankSWIFT": "string",
          "bankSWIFT2": "string",
          "city": "string",
          "code": "string",
          "companyName": "Ava Chen",
          "companyTypeID": 1,
          "country": "string",
          "defaultClientID": 1,
          "defaultCurrency": "string",
          "eInvoiceAddress": "string",
          "email": "ava@example.com",
          "fax": "string",
          "id": "string",
          "intermediatorCode": "string",
          "invoiceRounding": 1,
          "mobile": "string",
          "name": "Ava Chen",
          "phone": "string",
          "state": "string",
          "street": "string",
          "VAT": "string",
          "web": "string",
          "ZIPcode": "string"
        }
      ],
      "status": {
        "errorCode": 1,
        "generationTime": 1,
        "recordsInResponse": 1,
        "recordsTotal": 1,
        "request": "string",
        "requestUnixTime": 1,
        "responseStatus": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Company Info action reference](actions/get-company-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eRPLYBooks/latest/actions/get-company-info).
