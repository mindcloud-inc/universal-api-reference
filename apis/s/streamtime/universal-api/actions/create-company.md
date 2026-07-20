# Streamtime: Create Company



```
POST https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/create-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Streamtime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/create-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taxNumber": "NZ123-456-789"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/create-company', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taxNumber": "NZ123-456-789"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Company name Example: `Acme Corporation`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyStatus` | object | no | Status of a company |
| `companyStatus.id` | number | no | Company status ID Example: `1`. |
| `taxNumber` | string | yes | Tax/GST/VAT number Example: `NZ123-456-789`. |
| `phone1` | string | no | Primary phone number Example: `+64 9 123 4567`. |
| `phone2` | string | no | Secondary phone number Example: `+64 21 987 654`. |
| `websiteAddress` | string | no | Website URL Example: `https://www.acme.co`. |
| `physicalAddress` | object | no | Physical address object |
| `physicalAddress.line1` | string | no | Physical address line 1 Example: `123 High St`. |
| `physicalAddress.line2` | string | no | Physical address line 2 Example: `Suite 5`. |
| `physicalAddress.line3` | string | no | Physical address line 3 Example: `Building B`. |
| `physicalAddress.city` | string | no | Physical address city Example: `Auckland`. |
| `physicalAddress.region` | string | no | Physical address region Example: `Auckland`. |
| `physicalAddress.countryName` | string | no | Physical address country name Example: `New Zealand`. |
| `physicalAddress.postCode` | string | no | Physical address postal code Example: `1010`. |
| `postalAddress` | object | no | Postal address object |
| `postalAddress.line1` | string | no | Postal address line 1 Example: `PO Box 123`. |
| `postalAddress.line2` | string | no | Postal address line 2 Example: `Suite 5`. |
| `postalAddress.line3` | string | no | Postal address line 3 Example: `Building B`. |
| `postalAddress.city` | string | no | Postal address city Example: `Auckland`. |
| `postalAddress.region` | string | no | Postal address region Example: `Auckland`. |
| `postalAddress.countryName` | string | no | Postal address country name Example: `New Zealand`. |
| `postalAddress.postCode` | string | no | Postal address postal code Example: `1010`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "branchId": 1,
      "branchName": "Ava Chen",
      "companyLeadUserId": 1,
      "companyStatus": {},
      "id": 1,
      "name": "Ava Chen",
      "notes": "string",
      "phone1": "string",
      "phone2": "string",
      "rateCardId": 1,
      "taxNumber": "string",
      "websiteAddress": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `branchId` | number | Branch ID |
| `branchName` | string | Branch name |
| `companyLeadUserId` | number | Lead user ID |
| `companyStatus` | object | Company status |
| `id` | number | Company ID |
| `name` | string | Company name |
| `notes` | string | Notes |
| `phone1` | string | Primary phone number |
| `phone2` | string | Secondary phone number |
| `rateCardId` | number | Rate card ID |
| `taxNumber` | string | Tax number |
| `websiteAddress` | string | Website URL |

## Native endpoint

Through the native Streamtime API, this operation is `POST /companies` (base URL `https://api.streamtime.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-company.md) for the provider-specific parameters and requirements.

