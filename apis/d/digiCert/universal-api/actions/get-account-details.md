# DigiCert: Get Account Details

Retrieves your CertCentral account details from DigiCert.

```
GET https://connect.mindcloud.co/v1/universal/digiCert/latest/actions/get-account-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DigiCert `connectionId` ([setup](../authentication.md)).

## Example request

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



## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adminEmail` | string | Account admin email addresses. |
| `balanceNegativeLimit` | number | Negative balance limit. |
| `certCentralType` | string | CertCentral account type. |
| `certTransparency` | string | Certificate transparency behavior. |
| `displayRep` | boolean | Whether the account manager is shown in CertCentral. |
| `expressInstallEnabled` | boolean | Whether express install is enabled. |
| `id` | number | Account ID. |
| `isResellerCustomer` | boolean | Whether the account is a reseller customer. |
| `makeRenewalCalls` | boolean | Whether renewal calls are enabled. |
| `pricingModel` | string | Current pricing model. |
| `repEmail` | string | Account manager email. |
| `repName` | string | Account manager name. |
| `repPhone` | string | Account manager phone number. |

## Native endpoint

Through the native DigiCert API, this operation is `GET /account` (base URL `https://www.digicert.com/services/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-details.md) for the provider-specific parameters and requirements.

