# Zenoti: List Appointments By Guest



```
GET https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/list-appointments-by-guest
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenoti `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/list-appointments-by-guest?connectionId=$CONNECTION_ID&guestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "guestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/list-appointments-by-guest?${params}`, {
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
| `guestId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appointmentGroupId": "string",
      "appointmentServices": [
        {
          "actualStartTime": "2026-05-07T12:00:00.000Z",
          "addonAppointmentId": "string",
          "appointmentId": "string",
          "appointmentStatus": 1,
          "cartItemId": "string",
          "completedTime": "2026-05-07T12:00:00.000Z",
          "endTime": "2026-05-07T12:00:00.000Z",
          "equipment": "string",
          "hasSegments": true,
          "hasServiceForm": true,
          "invoiceItemId": "string",
          "isAddon": true,
          "isMembershipApplied": true,
          "itemActions": "string",
          "parentAppointmentId": "string",
          "progress": 1,
          "quantity": 1,
          "requestedTherapistGender": 1,
          "requestedTherapistId": "string",
          "room": "string",
          "segments": "string",
          "service": {
            "addons": {},
            "categoryId": "string",
            "displayName": {},
            "duration": 1,
            "hasAddons": {},
            "hasVariant": {},
            "id": "string",
            "isAddon": true,
            "isVariant": {},
            "name": "Ava Chen",
            "parentServiceId": {},
            "price": {
              "currencyId": 1,
              "final": 1,
              "sales": 1,
              "tax": 1
            }
          },
          "serviceCustomData": "string",
          "serviceCustomDataIndicator": "string",
          "startTime": "2026-05-07T12:00:00.000Z"
        }
      ],
      "centerId": "string",
      "checkCancelAndNoshow": true,
      "groupInvoiceId": "string",
      "invoiceId": "string",
      "invoiceStatus": 1,
      "isFeedbackSubmitted": true,
      "isRebooking": true,
      "noOfGuests": 1,
      "notes": "string",
      "price": {
        "currencyId": 1,
        "final": 1,
        "sales": 1,
        "tax": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appointmentGroupId` | string |  |
| `appointmentServices[].actualStartTime` | date |  |
| `appointmentServices[].addonAppointmentId` | string |  |
| `appointmentServices[].appointmentId` | string |  |
| `appointmentServices[].appointmentStatus` | number |  |
| `appointmentServices[].cartItemId` | string |  |
| `appointmentServices[].completedTime` | date |  |
| `appointmentServices[].endTime` | date |  |
| `appointmentServices[].equipment` | string |  |
| `appointmentServices[].hasSegments` | boolean |  |
| `appointmentServices[].hasServiceForm` | boolean |  |
| `appointmentServices[].invoiceItemId` | string |  |
| `appointmentServices[].isAddon` | boolean |  |
| `appointmentServices[].isMembershipApplied` | boolean |  |
| `appointmentServices[].itemActions` | string |  |
| `appointmentServices[].parentAppointmentId` | string |  |
| `appointmentServices[].progress` | number |  |
| `appointmentServices[].quantity` | number |  |
| `appointmentServices[].requestedTherapistGender` | number |  |
| `appointmentServices[].requestedTherapistId` | string |  |
| `appointmentServices[].room` | string |  |
| `appointmentServices[].segments` | string |  |
| `appointmentServices[].service.addons` | object |  |
| `appointmentServices[].service.categoryId` | string |  |
| `appointmentServices[].service.displayName` | object |  |
| `appointmentServices[].service.duration` | number |  |
| `appointmentServices[].service.hasAddons` | object |  |
| `appointmentServices[].service.hasVariant` | object |  |
| `appointmentServices[].service.id` | string |  |
| `appointmentServices[].service.isAddon` | boolean |  |
| `appointmentServices[].service.isVariant` | object |  |
| `appointmentServices[].service.name` | string |  |
| `appointmentServices[].service.parentServiceId` | object |  |
| `appointmentServices[].service.price.currencyId` | number |  |
| `appointmentServices[].service.price.final` | number |  |
| `appointmentServices[].service.price.sales` | number |  |
| `appointmentServices[].service.price.tax` | number |  |
| `appointmentServices[].serviceCustomData` | string |  |
| `appointmentServices[].serviceCustomDataIndicator` | string |  |
| `appointmentServices[].startTime` | date |  |
| `centerId` | string |  |
| `checkCancelAndNoshow` | boolean |  |
| `groupInvoiceId` | string |  |
| `invoiceId` | string |  |
| `invoiceStatus` | number |  |
| `isFeedbackSubmitted` | boolean |  |
| `isRebooking` | boolean |  |
| `noOfGuests` | number |  |
| `notes` | string |  |
| `price.currencyId` | number |  |
| `price.final` | number |  |
| `price.sales` | number |  |
| `price.tax` | number |  |

## Native endpoint

Through the native Zenoti API, this operation is `GET guests/:guestId/appointments` (base URL `https://api.zenoti.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-appointments-by-guest.md) for the provider-specific parameters and requirements.

