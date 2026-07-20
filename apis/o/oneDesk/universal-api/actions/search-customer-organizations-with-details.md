# OneDesk: Search Customer Organizations With Details

Finds customer organizations in OneDesk by filters, with details.

```
GET https://connect.mindcloud.co/v1/universal/oneDesk/latest/actions/search-customer-organizations-with-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneDesk/latest/actions/search-customer-organizations-with-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneDesk/latest/actions/search-customer-organizations-with-details?${params}`, {
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
| `properties[]` | array<object> | no | Array of OneDesk property filters. |
| `properties[].operation` | string | no | Comparison operation to apply to the property. |
| `properties[].property` | string | no | Name of property to be filtered. |
| `properties[].value` | string | no | Value used in the filter comparison. |
| `limit` | number | no | Maximum number of customer organization detail rows to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "externalId": "string",
      "invoicePreference": {
        "currencySymbol": {},
        "discount": {},
        "discountName": {},
        "email": {},
        "enablePrepaidHours": true,
        "firstName": {},
        "hoursPerPrepaidBlock": 1,
        "lastName": {},
        "overrideDefaultValue": {},
        "pricePerPrepaidBlock": 1,
        "remainingPrepaidHoursInMillis": {},
        "shipping": {},
        "shippingName": {},
        "tax1": {},
        "tax1Name": {},
        "tax2": {},
        "tax2Name": {}
      },
      "name": "Ava Chen",
      "profile": {
        "address": {},
        "city": {},
        "country": {},
        "description": {},
        "phone": {},
        "state": {},
        "zipCode": {}
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `externalId` | string |  |
| `invoicePreference.currencySymbol` | object |  |
| `invoicePreference.discount` | object |  |
| `invoicePreference.discountName` | object |  |
| `invoicePreference.email` | object |  |
| `invoicePreference.enablePrepaidHours` | boolean |  |
| `invoicePreference.firstName` | object |  |
| `invoicePreference.hoursPerPrepaidBlock` | number |  |
| `invoicePreference.lastName` | object |  |
| `invoicePreference.overrideDefaultValue` | object |  |
| `invoicePreference.pricePerPrepaidBlock` | number |  |
| `invoicePreference.remainingPrepaidHoursInMillis` | object |  |
| `invoicePreference.shipping` | object |  |
| `invoicePreference.shippingName` | object |  |
| `invoicePreference.tax1` | object |  |
| `invoicePreference.tax1Name` | object |  |
| `invoicePreference.tax2` | object |  |
| `invoicePreference.tax2Name` | object |  |
| `name` | string |  |
| `profile.address` | object |  |
| `profile.city` | object |  |
| `profile.country` | object |  |
| `profile.description` | object |  |
| `profile.phone` | object |  |
| `profile.state` | object |  |
| `profile.zipCode` | object |  |

## Native endpoint

Through the native OneDesk API, this operation is `POST /rest/public/customer-organizations/filter/details` (base URL `https://app.onedesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-customer-organizations-with-details.md) for the provider-specific parameters and requirements.

