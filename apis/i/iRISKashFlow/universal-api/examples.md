# IRIS KashFlow Universal API Examples

These examples use the MindCloud API key and IRIS KashFlow connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Company Details



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iRISKashFlow/latest/actions/get-company-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iRISKashFlow/latest/actions/get-company-details?${params}`, {
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
      "Address1": "string",
      "Address2": "string",
      "Address3": "string",
      "Address4": "string",
      "BusinessType": "string",
      "BusinessType1": "string",
      "BusinessType1Name": "Ava Chen",
      "BusinessType2": "string",
      "BusinessType2Name": "Ava Chen",
      "BusinessType3": "string",
      "BusinessType3Name": "Ava Chen",
      "CompanyName": "Ava Chen",
      "CurrencyId": "string",
      "CurrencyName": "Ava Chen",
      "CurrencyPosition": "string",
      "CurrencySymbol": "string",
      "Mobile": "string",
      "PaymentTerms": "string",
      "PaymentTermsType": "string",
      "Postcode": "string",
      "PrimaryContact": "string",
      "PrimaryEmail": "ava@example.com",
      "Telephone": "string",
      "UsDate": "string",
      "VatRegistered": "string",
      "VatRegistrationNumber": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Company Details action reference](actions/get-company-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/iRISKashFlow/latest/actions/get-company-details).
