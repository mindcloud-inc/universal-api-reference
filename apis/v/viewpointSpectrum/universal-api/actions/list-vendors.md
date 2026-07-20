# Viewpoint Spectrum: List Vendors



```
GET https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/list-vendors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Spectrum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/list-vendors?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/list-vendors?${params}`, {
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
| `pCity` | string | no |  |
| `pCostCenter` | string | no |  |
| `pName` | string | no |  |
| `pState` | string | no |  |
| `pType` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountReference": "string",
      "address1": "string",
      "address2": "string",
      "city": "string",
      "companyCode": "string",
      "discountPercent": 1,
      "discountTermDays": 1,
      "discountTerms": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "lastName": "Chen",
      "name": "Ava Chen",
      "paymentAddress1": "string",
      "paymentAddress2": "string",
      "paymentCity": "string",
      "paymentLocationName": "Ava Chen",
      "paymentState": "string",
      "paymentTermDays": 1,
      "paymentTerms": "string",
      "paymentZip": "string",
      "phone": "string",
      "purchaseAddress1": "string",
      "purchaseAddress2": "string",
      "purchaseCity": "string",
      "purchaseLocationName": "Ava Chen",
      "purchaseState": "string",
      "purchaseZip": "string",
      "state": "string",
      "vendorCode": "string",
      "zipCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountReference` | string |  |
| `address1` | string |  |
| `address2` | string |  |
| `city` | string |  |
| `companyCode` | string |  |
| `discountPercent` | number |  |
| `discountTermDays` | number |  |
| `discountTerms` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `lastName` | string |  |
| `name` | string |  |
| `paymentAddress1` | string |  |
| `paymentAddress2` | string |  |
| `paymentCity` | string |  |
| `paymentLocationName` | string |  |
| `paymentState` | string |  |
| `paymentTermDays` | number |  |
| `paymentTerms` | string |  |
| `paymentZip` | string |  |
| `phone` | string |  |
| `purchaseAddress1` | string |  |
| `purchaseAddress2` | string |  |
| `purchaseCity` | string |  |
| `purchaseLocationName` | string |  |
| `purchaseState` | string |  |
| `purchaseZip` | string |  |
| `state` | string |  |
| `vendorCode` | string |  |
| `zipCode` | string |  |

## Native endpoint

Through the native Viewpoint Spectrum API, this operation is `GET vendors/{{credentials.companyID}}` (base URL `{{credentials.url}}:8482/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-vendors.md) for the provider-specific parameters and requirements.

