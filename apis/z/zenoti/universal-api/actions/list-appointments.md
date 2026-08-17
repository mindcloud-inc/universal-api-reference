# Zenoti: List Appointments



```
GET https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/list-appointments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenoti `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/list-appointments?connectionId=$CONNECTION_ID&centerId=string&startDate=2026-05-07T12%3A00%3A00.000Z&endDate=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "centerId": "string",
  "startDate": "2026-05-07T12:00:00.000Z",
  "endDate": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/list-appointments?${params}`, {
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
| `centerId` | list | yes |  |
| `startDate` | date | yes |  |
| `endDate` | date | yes | Retrieves the appointments that have appointment start date before the specified end_date (exclusive of end_date). For example, if you specify start_date as 2020-08-03 and end_date as 2020-08-04, this API will retrieve the list of appointments for only Aug 3, 2020. Note: start_date and end_date must be different. |
| `includeNoShowsCancelled` | boolean | no | Default: `false`. |
| `therapistId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actualCompletedTime": "string",
      "actualStartTime": "string",
      "appCount": 1,
      "appointmentCategoryId": "string",
      "appointmentGroupId": "string",
      "appointmentId": "string",
      "appointmentSegmentId": "string",
      "appointmentType": 1,
      "areCustomFieldsFilled": true,
      "arePackageTargetsFilled": true,
      "arePackageTargetsRequired": true,
      "autoPayAuthorizeStatus": 1,
      "availableRooms": "string",
      "availableTherapists": "string",
      "availableTimes": "string",
      "blockout": "string",
      "cancelOrNoShowStatus": 1,
      "canUpdateTherapist": true,
      "checkinTime": "2026-05-07T12:00:00.000Z",
      "closedById": "string",
      "createdById": "string",
      "creationDate": "2026-05-07T12:00:00.000Z",
      "creationDateUtc": "2026-05-07T12:00:00.000Z",
      "emailLink": "ava@example.com",
      "endTime": "2026-05-07T12:00:00.000Z",
      "endTimeUtc": "2026-05-07T12:00:00.000Z",
      "equipment": "string",
      "error": "string",
      "formId": "string",
      "groupInvoiceId": "string",
      "groupName": "Ava Chen",
      "groupNotes": "string",
      "guest": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "gender": 1,
        "guestIndicatorValue": {
          "autoPayEnabled": {},
          "cardOnFile": {},
          "customDataIndicator": {},
          "dues": {},
          "firstTimer": {},
          "guestIconInformation": {},
          "hasActivePackages": {},
          "hasAddOns": {},
          "hasCTA": {},
          "hasFrozenPackages": {},
          "hasProfileAlerts": {},
          "highSpender": {},
          "isGuestBirthday": {},
          "isMinor": {},
          "isSurpriseVisit": {},
          "lowFeedback": {},
          "lpTier": {},
          "member": 1,
          "nonExpireandNotClosedPackages": {},
          "nonExpirePackages": {},
          "noShow": {},
          "otherCenterGuest": {},
          "rebookedAppointment": {},
          "recurrenceAppointment": {},
          "regularGuest": {},
          "returningCustomer": {},
          "showGuestNotes": {}
        },
        "id": "string",
        "indicator": "string",
        "isVirtualUser": true,
        "lastName": "Chen",
        "lpTierInfo": "string",
        "mobile": {
          "countryId": 1,
          "displayNumber": "string",
          "number": {}
        },
        "preferredPronoun": "string"
      },
      "hasActiveMembershipForAutoPay": true,
      "hasUnexpiredPackages": true,
      "hasVirtualUserSiblings": true,
      "invoiceId": "string",
      "invoiceItemId": "string",
      "invoiceLocked": true,
      "invoiceProcessedInIntegrations": 1,
      "isBlocked": true,
      "isEducatorRatingFilled": true,
      "isFeedbackFilled": true,
      "isPrescriptionSigned": true,
      "isProductConsumptionUpdated": true,
      "isServiceBundleDayPackage": true,
      "isSingleAppointment": true,
      "locked": true,
      "notes": "string",
      "packageId": "string",
      "packageName": "Ava Chen",
      "parallelGroupId": "string",
      "parentServiceName": "Ava Chen",
      "price": {
        "currencyId": 1,
        "discount": 1,
        "final": 1,
        "final1": 1,
        "roundingCorrection": 1,
        "sales": 1,
        "ssg": {},
        "tax": 1,
        "tip": 1
      },
      "progress": 1,
      "quantity": 1,
      "requestedAlternative": 1,
      "room": "string",
      "selectedRoomId": "string",
      "selectedTherapistId": "string",
      "selectedTime": "2026-05-07T12:00:00.000Z",
      "service": {
        "businessUnit": {
          "guid": "string",
          "id": 1,
          "name": "Ava Chen"
        },
        "category": {
          "id": "string",
          "name": "Ava Chen"
        },
        "hasAddons": true,
        "id": "string",
        "isAddon": true,
        "isVirtualService": true,
        "name": "Ava Chen",
        "overrideDefaultProductConsumption": true,
        "overrideProductConsumption": true,
        "parentAppointmentId": {},
        "segmentId": "string",
        "subCategory": {
          "id": "string",
          "name": "Ava Chen"
        }
      },
      "serviceCustomDataIndicator": "string",
      "showInCalender": 1,
      "smsLink": "https://example.com",
      "source": 1,
      "startTime": "2026-05-07T12:00:00.000Z",
      "startTimeUtc": "2026-05-07T12:00:00.000Z",
      "status": 1,
      "therapist": {
        "displayName": {},
        "email": "ava@example.com",
        "firstName": "Ava",
        "gender": 1,
        "id": "string",
        "lastName": "Chen",
        "nickName": {},
        "vanityImageUrl": "https://example.com"
      },
      "therapistPreferenceType": 1,
      "virtualRoomLink": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actualCompletedTime` | string |  |
| `actualStartTime` | string |  |
| `appCount` | number |  |
| `appointmentCategoryId` | string |  |
| `appointmentGroupId` | string |  |
| `appointmentId` | string |  |
| `appointmentSegmentId` | string |  |
| `appointmentType` | number |  |
| `areCustomFieldsFilled` | boolean |  |
| `arePackageTargetsFilled` | boolean |  |
| `arePackageTargetsRequired` | boolean |  |
| `autoPayAuthorizeStatus` | number |  |
| `availableRooms` | string |  |
| `availableTherapists` | string |  |
| `availableTimes` | string |  |
| `blockout` | string |  |
| `cancelOrNoShowStatus` | number |  |
| `canUpdateTherapist` | boolean |  |
| `checkinTime` | date |  |
| `closedById` | string |  |
| `createdById` | string |  |
| `creationDate` | date |  |
| `creationDateUtc` | date |  |
| `emailLink` | string |  |
| `endTime` | date |  |
| `endTimeUtc` | date |  |
| `equipment` | string |  |
| `error` | string |  |
| `formId` | string |  |
| `groupInvoiceId` | string |  |
| `groupName` | string |  |
| `groupNotes` | string |  |
| `guest.email` | string |  |
| `guest.firstName` | string |  |
| `guest.gender` | number |  |
| `guest.guestIndicatorValue.autoPayEnabled` | object |  |
| `guest.guestIndicatorValue.cardOnFile` | object |  |
| `guest.guestIndicatorValue.customDataIndicator` | object |  |
| `guest.guestIndicatorValue.dues` | object |  |
| `guest.guestIndicatorValue.firstTimer` | object |  |
| `guest.guestIndicatorValue.guestIconInformation` | object |  |
| `guest.guestIndicatorValue.hasActivePackages` | object |  |
| `guest.guestIndicatorValue.hasAddOns` | object |  |
| `guest.guestIndicatorValue.hasCTA` | object |  |
| `guest.guestIndicatorValue.hasFrozenPackages` | object |  |
| `guest.guestIndicatorValue.hasProfileAlerts` | object |  |
| `guest.guestIndicatorValue.highSpender` | object |  |
| `guest.guestIndicatorValue.isGuestBirthday` | object |  |
| `guest.guestIndicatorValue.isMinor` | object |  |
| `guest.guestIndicatorValue.isSurpriseVisit` | object |  |
| `guest.guestIndicatorValue.lowFeedback` | object |  |
| `guest.guestIndicatorValue.lpTier` | object |  |
| `guest.guestIndicatorValue.member` | number |  |
| `guest.guestIndicatorValue.nonExpireandNotClosedPackages` | object |  |
| `guest.guestIndicatorValue.nonExpirePackages` | object |  |
| `guest.guestIndicatorValue.noShow` | object |  |
| `guest.guestIndicatorValue.otherCenterGuest` | object |  |
| `guest.guestIndicatorValue.rebookedAppointment` | object |  |
| `guest.guestIndicatorValue.recurrenceAppointment` | object |  |
| `guest.guestIndicatorValue.regularGuest` | object |  |
| `guest.guestIndicatorValue.returningCustomer` | object |  |
| `guest.guestIndicatorValue.showGuestNotes` | object |  |
| `guest.id` | string |  |
| `guest.indicator` | string |  |
| `guest.isVirtualUser` | boolean |  |
| `guest.lastName` | string |  |
| `guest.lpTierInfo` | string |  |
| `guest.mobile.countryId` | number |  |
| `guest.mobile.displayNumber` | string |  |
| `guest.mobile.number` | object |  |
| `guest.preferredPronoun` | string |  |
| `hasActiveMembershipForAutoPay` | boolean |  |
| `hasUnexpiredPackages` | boolean |  |
| `hasVirtualUserSiblings` | boolean |  |
| `invoiceId` | string |  |
| `invoiceItemId` | string |  |
| `invoiceLocked` | boolean |  |
| `invoiceProcessedInIntegrations` | number |  |
| `isBlocked` | boolean |  |
| `isEducatorRatingFilled` | boolean |  |
| `isFeedbackFilled` | boolean |  |
| `isPrescriptionSigned` | boolean |  |
| `isProductConsumptionUpdated` | boolean |  |
| `isServiceBundleDayPackage` | boolean |  |
| `isSingleAppointment` | boolean |  |
| `locked` | boolean |  |
| `notes` | string |  |
| `packageId` | string |  |
| `packageName` | string |  |
| `parallelGroupId` | string |  |
| `parentServiceName` | string |  |
| `price.currencyId` | number |  |
| `price.discount` | number |  |
| `price.final` | number |  |
| `price.final1` | number |  |
| `price.roundingCorrection` | number |  |
| `price.sales` | number |  |
| `price.ssg` | object |  |
| `price.tax` | number |  |
| `price.tip` | number |  |
| `progress` | number |  |
| `quantity` | number |  |
| `requestedAlternative` | number |  |
| `room` | string |  |
| `selectedRoomId` | string |  |
| `selectedTherapistId` | string |  |
| `selectedTime` | date |  |
| `service.businessUnit.guid` | string |  |
| `service.businessUnit.id` | number |  |
| `service.businessUnit.name` | string |  |
| `service.category.id` | string |  |
| `service.category.name` | string |  |
| `service.hasAddons` | boolean |  |
| `service.id` | string |  |
| `service.isAddon` | boolean |  |
| `service.isVirtualService` | boolean |  |
| `service.name` | string |  |
| `service.overrideDefaultProductConsumption` | boolean |  |
| `service.overrideProductConsumption` | boolean |  |
| `service.parentAppointmentId` | object |  |
| `service.segmentId` | string |  |
| `service.subCategory.id` | string |  |
| `service.subCategory.name` | string |  |
| `serviceCustomDataIndicator` | string |  |
| `showInCalender` | number |  |
| `smsLink` | string |  |
| `source` | number |  |
| `startTime` | date |  |
| `startTimeUtc` | date |  |
| `status` | number |  |
| `therapist.displayName` | object |  |
| `therapist.email` | string |  |
| `therapist.firstName` | string |  |
| `therapist.gender` | number |  |
| `therapist.id` | string |  |
| `therapist.lastName` | string |  |
| `therapist.nickName` | object |  |
| `therapist.vanityImageUrl` | string |  |
| `therapistPreferenceType` | number |  |
| `virtualRoomLink` | string |  |

## Native endpoint

Through the native Zenoti API, this operation is `GET appointments` (base URL `https://api.zenoti.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-appointments.md) for the provider-specific parameters and requirements.

