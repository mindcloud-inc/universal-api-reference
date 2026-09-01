# Zenoti Universal API Examples

These examples use the MindCloud API key and Zenoti connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Centers

This API retrieves an organization's list of active centers.

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

Example response:

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

See the full [List Centers action reference](actions/list-centers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zenoti/latest/actions/list-centers).
