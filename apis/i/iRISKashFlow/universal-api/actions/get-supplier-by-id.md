# IRIS KashFlow: Get Supplier by ID



```
GET https://connect.mindcloud.co/v1/universal/iRISKashFlow/latest/actions/get-supplier-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IRIS KashFlow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iRISKashFlow/latest/actions/get-supplier-by-id?connectionId=$CONNECTION_ID&supplierId=12473072" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "supplierId": "12473072"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iRISKashFlow/latest/actions/get-supplier-by-id?${params}`, {
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
| `supplierId` | number | yes | Default: `12473072`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address1": "string",
      "address2": "string",
      "address3": "string",
      "address4": "string",
      "code": "string",
      "contact": "string",
      "contactFirstName": "Ava",
      "contactLastName": "Chen",
      "contactTitle": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "currencyID": "string",
      "eC": "string",
      "email": "ava@example.com",
      "fax": "string",
      "mobile": "string",
      "name": "Ava Chen",
      "notes": "string",
      "paymentTerms": "string",
      "postCode": "string",
      "supplierID": "string",
      "telephone": "string",
      "tradeBorderType": "string",
      "updated": "2026-05-07T12:00:00.000Z",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address1` | string |  |
| `address2` | string |  |
| `address3` | string |  |
| `address4` | string |  |
| `code` | string |  |
| `contact` | string |  |
| `contactFirstName` | string |  |
| `contactLastName` | string |  |
| `contactTitle` | string |  |
| `created` | date |  |
| `currencyID` | string |  |
| `eC` | string |  |
| `email` | string |  |
| `fax` | string |  |
| `mobile` | string |  |
| `name` | string |  |
| `notes` | string |  |
| `paymentTerms` | string |  |
| `postCode` | string |  |
| `supplierID` | string |  |
| `telephone` | string |  |
| `tradeBorderType` | string |  |
| `updated` | date |  |
| `website` | string |  |

## Native endpoint

Through the native IRIS KashFlow API, this operation is `POST /api/service.asmx` (base URL `https://securedwebapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-supplier-by-id.md) for the provider-specific parameters and requirements.

