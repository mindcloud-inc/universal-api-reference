# DigiCert Universal API Examples

These examples use the MindCloud API key and DigiCert connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Details

Retrieves your CertCentral account details from DigiCert.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digiCert/latest/actions/get-account-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digiCert/latest/actions/get-account-details?${params}`, {
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
      "adminEmail": "ava@example.com",
      "balanceNegativeLimit": 1,
      "certCentralType": "string",
      "certTransparency": "string",
      "displayRep": true,
      "expressInstallEnabled": true,
      "id": 1,
      "isResellerCustomer": true,
      "makeRenewalCalls": true,
      "pricingModel": "string",
      "repEmail": "ava@example.com",
      "repName": "Ava Chen",
      "repPhone": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Account Details action reference](actions/get-account-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/digiCert/latest/actions/get-account-details).
