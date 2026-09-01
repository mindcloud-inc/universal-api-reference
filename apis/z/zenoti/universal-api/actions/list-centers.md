# Zenoti: List Centers

This API retrieves an organization's list of active centers.

```
GET https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/list-centers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenoti `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/list-centers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/list-centers?${params}`, {
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
      "additionalInfo": {
        "availableCategories": "string",
        "availableServices": "string",
        "canBook": true,
        "cancellationFeeDuration": 1,
        "categoriesAvailable": true,
        "centerAmenities": "string",
        "collectFeedback": "string",
        "cst": "string",
        "feedbackLabel": "string",
        "feedbackLink": "https://example.com",
        "isAddOnsAvailable": true,
        "isAutoPayEnabledAtCenter": true,
        "isCenterAmenitiesEnabled": true,
        "isGlobalTokenizationSupported": true,
        "servicesAvailable": true,
        "serviceTaxNo": "string",
        "tin": "string",
        "unavailableCategories": "string",
        "unavailableServices": "string",
        "vat": "string"
      },
      "addressInfo": {
        "address1": "string",
        "address2": "string",
        "city": "Ava Chen",
        "zipCode": "string"
      },
      "code": "string",
      "contactInfo": {
        "email": "ava@example.com",
        "phone1": {
          "countryId": 1,
          "displayNumber": "string",
          "number": "string"
        },
        "phone2": {
          "countryId": 1,
          "displayNumber": "string",
          "number": "string"
        }
      },
      "country": {
        "code": "string",
        "id": 1,
        "name": "Ava Chen",
        "nationality": "string",
        "phoneCode": 1
      },
      "cultureCodeAtCenter": "string",
      "currency": {
        "code": "string",
        "id": 1,
        "name": "Ava Chen",
        "symbol": "string"
      },
      "description": "string",
      "displayName": "Ava Chen",
      "enableParallelServicesAtCenter": true,
      "id": "string",
      "isFbeEnabled": true,
      "isHcCallCenter": true,
      "location": {
        "latitude": 1,
        "lattitude": 1,
        "longitude": 1,
        "timeZone": {
          "id": 1,
          "name": "Ava Chen",
          "standardName": "Ava Chen",
          "symbol": "string"
        }
      },
      "name": "Ava Chen",
      "onlineBookingStartDate": "2026-05-07T12:00:00.000Z",
      "settings": "string",
      "state": {
        "code": "string",
        "id": 1,
        "name": "Ava Chen",
        "shortName": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `additionalInfo.availableCategories` | string |  |
| `additionalInfo.availableServices` | string |  |
| `additionalInfo.canBook` | boolean |  |
| `additionalInfo.cancellationFeeDuration` | number |  |
| `additionalInfo.categoriesAvailable` | boolean |  |
| `additionalInfo.centerAmenities` | string |  |
| `additionalInfo.collectFeedback` | string |  |
| `additionalInfo.cst` | string |  |
| `additionalInfo.feedbackLabel` | string |  |
| `additionalInfo.feedbackLink` | string |  |
| `additionalInfo.isAddOnsAvailable` | boolean |  |
| `additionalInfo.isAutoPayEnabledAtCenter` | boolean |  |
| `additionalInfo.isCenterAmenitiesEnabled` | boolean |  |
| `additionalInfo.isGlobalTokenizationSupported` | boolean |  |
| `additionalInfo.servicesAvailable` | boolean |  |
| `additionalInfo.serviceTaxNo` | string |  |
| `additionalInfo.tin` | string |  |
| `additionalInfo.unavailableCategories` | string |  |
| `additionalInfo.unavailableServices` | string |  |
| `additionalInfo.vat` | string |  |
| `addressInfo.address1` | string |  |
| `addressInfo.address2` | string |  |
| `addressInfo.city` | string |  |
| `addressInfo.zipCode` | string |  |
| `code` | string |  |
| `contactInfo.email` | string |  |
| `contactInfo.phone1.countryId` | number |  |
| `contactInfo.phone1.displayNumber` | string |  |
| `contactInfo.phone1.number` | string |  |
| `contactInfo.phone2.countryId` | number |  |
| `contactInfo.phone2.displayNumber` | string |  |
| `contactInfo.phone2.number` | string |  |
| `country.code` | string |  |
| `country.id` | number |  |
| `country.name` | string |  |
| `country.nationality` | string |  |
| `country.phoneCode` | number |  |
| `cultureCodeAtCenter` | string |  |
| `currency.code` | string |  |
| `currency.id` | number |  |
| `currency.name` | string |  |
| `currency.symbol` | string |  |
| `description` | string |  |
| `displayName` | string |  |
| `enableParallelServicesAtCenter` | boolean |  |
| `id` | string |  |
| `isFbeEnabled` | boolean |  |
| `isHcCallCenter` | boolean |  |
| `location.latitude` | number |  |
| `location.lattitude` | number |  |
| `location.longitude` | number |  |
| `location.timeZone.id` | number |  |
| `location.timeZone.name` | string |  |
| `location.timeZone.standardName` | string |  |
| `location.timeZone.symbol` | string |  |
| `name` | string |  |
| `onlineBookingStartDate` | date |  |
| `settings` | string |  |
| `state.code` | string |  |
| `state.id` | number |  |
| `state.name` | string |  |
| `state.shortName` | string |  |

## Native endpoint

Through the native Zenoti API, this operation is `GET centers` (base URL `https://api.zenoti.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-centers.md) for the provider-specific parameters and requirements.

