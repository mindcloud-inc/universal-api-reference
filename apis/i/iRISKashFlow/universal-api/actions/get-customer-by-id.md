# IRIS KashFlow: Get Customer by ID



```
GET https://connect.mindcloud.co/v1/universal/iRISKashFlow/latest/actions/get-customer-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IRIS KashFlow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iRISKashFlow/latest/actions/get-customer-by-id?connectionId=$CONNECTION_ID&customerId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iRISKashFlow/latest/actions/get-customer-by-id?${params}`, {
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
| `customerId` | number | yes |  |

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
      "checkBox1": "string",
      "checkBox10": "string",
      "checkBox11": "string",
      "checkBox12": "string",
      "checkBox13": "string",
      "checkBox14": "string",
      "checkBox15": "string",
      "checkBox16": "string",
      "checkBox17": "string",
      "checkBox18": "string",
      "checkBox19": "string",
      "checkBox2": "string",
      "checkBox20": "string",
      "checkBox3": "string",
      "checkBox4": "string",
      "checkBox5": "string",
      "checkBox6": "string",
      "checkBox7": "string",
      "checkBox8": "string",
      "checkBox9": "string",
      "code": "string",
      "contact": "string",
      "contactFirstName": "Ava",
      "contactLastName": "Chen",
      "contactTitle": "string",
      "countryCode": "string",
      "countryName": "Ava Chen",
      "created": "2026-05-07T12:00:00.000Z",
      "currencyID": "string",
      "custHasDeliveryAddress": "string",
      "customerID": "string",
      "deliveryAddress1": "string",
      "deliveryAddress2": "string",
      "deliveryAddress3": "string",
      "deliveryAddress4": "string",
      "deliveryCountryCode": "string",
      "deliveryCountryName": "Ava Chen",
      "deliveryPostcode": "string",
      "discount": "string",
      "eC": "string",
      "email": "ava@example.com",
      "extraText1": "string",
      "extraText10": "string",
      "extraText11": "string",
      "extraText12": "string",
      "extraText13": "string",
      "extraText14": "string",
      "extraText15": "string",
      "extraText16": "string",
      "extraText17": "string",
      "extraText18": "string",
      "extraText19": "string",
      "extraText2": "string",
      "extraText20": "string",
      "extraText3": "string",
      "extraText4": "string",
      "extraText5": "string",
      "extraText6": "string",
      "extraText7": "string",
      "extraText8": "string",
      "extraText9": "string",
      "fax": "string",
      "mobile": "string",
      "name": "Ava Chen",
      "notes": "string",
      "outsideEC": "string",
      "paymentTerms": "string",
      "postcode": "string",
      "showDiscount": "string",
      "source": "string",
      "telephone": "string",
      "updated": "string",
      "vATNumber": "string",
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
| `checkBox1` | string |  |
| `checkBox10` | string |  |
| `checkBox11` | string |  |
| `checkBox12` | string |  |
| `checkBox13` | string |  |
| `checkBox14` | string |  |
| `checkBox15` | string |  |
| `checkBox16` | string |  |
| `checkBox17` | string |  |
| `checkBox18` | string |  |
| `checkBox19` | string |  |
| `checkBox2` | string |  |
| `checkBox20` | string |  |
| `checkBox3` | string |  |
| `checkBox4` | string |  |
| `checkBox5` | string |  |
| `checkBox6` | string |  |
| `checkBox7` | string |  |
| `checkBox8` | string |  |
| `checkBox9` | string |  |
| `code` | string |  |
| `contact` | string |  |
| `contactFirstName` | string |  |
| `contactLastName` | string |  |
| `contactTitle` | string |  |
| `countryCode` | string |  |
| `countryName` | string |  |
| `created` | date |  |
| `currencyID` | string |  |
| `custHasDeliveryAddress` | string |  |
| `customerID` | string |  |
| `deliveryAddress1` | string |  |
| `deliveryAddress2` | string |  |
| `deliveryAddress3` | string |  |
| `deliveryAddress4` | string |  |
| `deliveryCountryCode` | string |  |
| `deliveryCountryName` | string |  |
| `deliveryPostcode` | string |  |
| `discount` | string |  |
| `eC` | string |  |
| `email` | string |  |
| `extraText1` | string |  |
| `extraText10` | string |  |
| `extraText11` | string |  |
| `extraText12` | string |  |
| `extraText13` | string |  |
| `extraText14` | string |  |
| `extraText15` | string |  |
| `extraText16` | string |  |
| `extraText17` | string |  |
| `extraText18` | string |  |
| `extraText19` | string |  |
| `extraText2` | string |  |
| `extraText20` | string |  |
| `extraText3` | string |  |
| `extraText4` | string |  |
| `extraText5` | string |  |
| `extraText6` | string |  |
| `extraText7` | string |  |
| `extraText8` | string |  |
| `extraText9` | string |  |
| `fax` | string |  |
| `mobile` | string |  |
| `name` | string |  |
| `notes` | string |  |
| `outsideEC` | string |  |
| `paymentTerms` | string |  |
| `postcode` | string |  |
| `showDiscount` | string |  |
| `source` | string |  |
| `telephone` | string |  |
| `updated` | string |  |
| `vATNumber` | string |  |
| `website` | string |  |

## Native endpoint

Through the native IRIS KashFlow API, this operation is `POST /api/service.asmx` (base URL `https://securedwebapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer-by-id.md) for the provider-specific parameters and requirements.

