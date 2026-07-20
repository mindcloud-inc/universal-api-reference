# OneDesk: Get Customer Organization By External ID

Retrieves a customer organization by external ID from OneDesk.

```
GET https://connect.mindcloud.co/v1/universal/oneDesk/latest/actions/get-customer-organization-by-external-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneDesk/latest/actions/get-customer-organization-by-external-id?connectionId=$CONNECTION_ID&externalId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "externalId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneDesk/latest/actions/get-customer-organization-by-external-id?${params}`, {
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
| `externalId` | string | yes | External ID of the customer organization. |

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

Through the native OneDesk API, this operation is `GET /rest/public/customer-organizations/externalId/:externalId` (base URL `https://app.onedesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer-organization-by-external-id.md) for the provider-specific parameters and requirements.

