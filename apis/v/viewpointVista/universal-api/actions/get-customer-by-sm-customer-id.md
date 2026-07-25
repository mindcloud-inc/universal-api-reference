# Viewpoint Vista: Get Customer by SMCustomerID

Represents Info, Contacts and Notes tabs data found in Viewpoint® Vista™ SM Customer program.

```
GET https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/get-customer-by-sm-customer-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Vista `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/get-customer-by-sm-customer-id?connectionId=$CONNECTION_ID&SMCustomerID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "SMCustomerID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/get-customer-by-sm-customer-id?${params}`, {
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
| `SMCustomerID` | string | yes | The SMCustomerID portion of the key used to identify the object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": "string",
      "altBillAddr": 1,
      "billingAddress1": "string",
      "billingAddress2": "string",
      "billingCity": "string",
      "billingCountry": "string",
      "billingEmail": "ava@example.com",
      "billingName": "Ava Chen",
      "billingPostalCode": "string",
      "billingState": "string",
      "billToARCustomer": 1,
      "contacts": [
        {
          "contactGroup": 1,
          "contactSeq": 1
        }
      ],
      "custGroup": 1,
      "customer": 1,
      "customerPOSetting": "string",
      "deliveryMethod": "string",
      "deliveryTo": "string",
      "invoiceGrouping": "string",
      "invoiceGroupingPOOverride": "string",
      "invoiceSummaryLevel": "string",
      "ModifiedUTC": "string",
      "nonBillable": "string",
      "notes": "string",
      "primaryTechnician": "string",
      "rateTemplate": "string",
      "reportID": 1,
      "reviewer": "string",
      "RyvitKeys": "string",
      "sMCo": 1,
      "sMCustomerID": 1,
      "uniqueAttchID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | string |  |
| `altBillAddr` | number |  |
| `billingAddress1` | string |  |
| `billingAddress2` | string |  |
| `billingCity` | string |  |
| `billingCountry` | string |  |
| `billingEmail` | string |  |
| `billingName` | string |  |
| `billingPostalCode` | string |  |
| `billingState` | string |  |
| `billToARCustomer` | number |  |
| `contacts[].contactGroup` | number |  |
| `contacts[].contactSeq` | number |  |
| `custGroup` | number |  |
| `customer` | number |  |
| `customerPOSetting` | string |  |
| `deliveryMethod` | string |  |
| `deliveryTo` | string |  |
| `invoiceGrouping` | string |  |
| `invoiceGroupingPOOverride` | string |  |
| `invoiceSummaryLevel` | string |  |
| `ModifiedUTC` | string |  |
| `nonBillable` | string |  |
| `notes` | string |  |
| `primaryTechnician` | string |  |
| `rateTemplate` | string |  |
| `reportID` | number |  |
| `reviewer` | string |  |
| `RyvitKeys` | string |  |
| `sMCo` | number |  |
| `sMCustomerID` | number |  |
| `uniqueAttchID` | string |  |

## Native endpoint

Through the native Viewpoint Vista API, this operation is `GET v1/direct/subscribers/:subscriber_code/vista/sm/2/data/customers/cache/id/:SMCustomerID` (base URL `https://api.xchange.trimble.com/connect/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer-by-sm-customer-id.md) for the provider-specific parameters and requirements.

