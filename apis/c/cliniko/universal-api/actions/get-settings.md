# Cliniko: Get Settings

Retrieves settings from your Cliniko account.

```
GET https://connect.mindcloud.co/v1/universal/cliniko/latest/actions/get-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cliniko `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cliniko/latest/actions/get-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cliniko/latest/actions/get-settings?${params}`, {
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
      "account": {
        "admin": {
          "email": "ava@example.com",
          "firstName": "Ava",
          "lastName": "Chen"
        },
        "compliance": {
          "hasHipaaComplianceConflicts": true,
          "hipaaComplianceConflictMessages": [
            "string"
          ]
        },
        "country": "string",
        "countryCode": "string",
        "currencySymbol": "string",
        "emailFrom": "ava@example.com",
        "hasTimeTravelers": true,
        "id": "string",
        "includePatientDobOnInvoice": true,
        "invoiceCalculationMethod": 1,
        "invoiceCalculationMethodDescription": "string",
        "invoiceDefaultNotes": {},
        "invoiceTitle": "string",
        "legalAccountName": "Ava Chen",
        "name": "Ava Chen",
        "requiresTfa": true,
        "subdomain": "string",
        "timeZone": "string",
        "timeZoneIdentifier": "string",
        "timeZoneSupport": true
      },
      "calendar": {
        "endHour": 1,
        "multipleAppointmentsGap": true,
        "showCurrentTimeIndicator": true,
        "startHour": 1,
        "timeslotHeightInPixels": 1,
        "timeslotSizeInMinutes": 1
      },
      "documentsAndPrinting": {
        "logoHeight": 1,
        "logoUrl": {}
      },
      "integrations": {
        "mailChimp": {
          "enabled": true
        },
        "medipass": {
          "enabled": true
        },
        "xero": {
          "enabled": {},
          "integratedForInvoices": {}
        }
      },
      "links": {
        "self": "https://example.com"
      },
      "onlineBookings": {
        "adroll": {
          "advertiserId": {},
          "pixelId": {}
        },
        "allowBookingsDaysInAdvance": 1,
        "allowOnlineBookingsTimeZoneChoice": true,
        "bookingReservationMinutes": 1,
        "calendarInfo": {},
        "dailyBookingsLimit": 1,
        "disabledText": {},
        "disabledTitle": {},
        "enabled": true,
        "googleAnalytics": {
          "trackingId": {}
        },
        "googleTagManager": {
          "containerId": {}
        },
        "logoUrl": {},
        "maxAppointmentsPerDaySegment": 1,
        "minHoursAdvanceRequiredToBook": 1,
        "minHoursNoticeForPatientCancellation": 1,
        "noticeEnabled": true,
        "noticeText": {},
        "noticeTitle": {},
        "notifyPractitionerByEmail": true,
        "notifyPractitionerBySms": true,
        "policy": {},
        "practitionerOrder": {},
        "privacyPolicyUrl": {},
        "requirePatientAddress": true,
        "showAppointmentDuration": true,
        "showPrices": true
      },
      "onlinePayments": {
        "activated": true
      },
      "patientCustomFieldsDefinition": {},
      "patientPrivacy": {
        "anonymiseAppointmentsOnDeletion": true,
        "anonymiseBookingNotifications": true,
        "anonymiseInvoicesAndPaymentsOnDeletion": true,
        "baaRequested": true,
        "browserTitleNameFormat": "Ava Chen",
        "icalPatientNameOption": "Ava Chen",
        "preventSendingFinancialDataByEmail": true,
        "requiresHipaaCompliance": true
      },
      "reminders": {
        "defaultRemindersCommunicationChannels": [
          1
        ],
        "defaultRemindersCommunicationChannelsDescription": "string",
        "defaultReminderType": "string"
      },
      "sms": {
        "alphanumericSourceNumberRequired": true,
        "defaultAlphanumericSourceNumber": "string",
        "maxMessageLength": {},
        "numberOfUsableCharactersPerMessage": 1,
        "repliesSupported": true
      },
      "terminology": {
        "addressCity": "string",
        "addressPostCode": "string",
        "addressState": "string",
        "patient": "string",
        "titles": [
          "string"
        ]
      },
      "waitList": {
        "defaultWaitListExpiryPeriod": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account.admin.email` | string |  |
| `account.admin.firstName` | string |  |
| `account.admin.lastName` | string |  |
| `account.compliance.hasHipaaComplianceConflicts` | boolean |  |
| `account.compliance.hipaaComplianceConflictMessages[]` | string |  |
| `account.country` | string |  |
| `account.countryCode` | string |  |
| `account.currencySymbol` | string |  |
| `account.emailFrom` | string |  |
| `account.hasTimeTravelers` | boolean |  |
| `account.id` | string |  |
| `account.includePatientDobOnInvoice` | boolean |  |
| `account.invoiceCalculationMethod` | number |  |
| `account.invoiceCalculationMethodDescription` | string |  |
| `account.invoiceDefaultNotes` | object |  |
| `account.invoiceTitle` | string |  |
| `account.legalAccountName` | string |  |
| `account.name` | string |  |
| `account.requiresTfa` | boolean |  |
| `account.subdomain` | string |  |
| `account.timeZone` | string |  |
| `account.timeZoneIdentifier` | string |  |
| `account.timeZoneSupport` | boolean |  |
| `calendar.endHour` | number |  |
| `calendar.multipleAppointmentsGap` | boolean |  |
| `calendar.showCurrentTimeIndicator` | boolean |  |
| `calendar.startHour` | number |  |
| `calendar.timeslotHeightInPixels` | number |  |
| `calendar.timeslotSizeInMinutes` | number |  |
| `documentsAndPrinting.logoHeight` | number |  |
| `documentsAndPrinting.logoUrl` | object |  |
| `integrations.mailChimp.enabled` | boolean |  |
| `integrations.medipass.enabled` | boolean |  |
| `integrations.xero.enabled` | object |  |
| `integrations.xero.integratedForInvoices` | object |  |
| `links.self` | string |  |
| `onlineBookings.adroll.advertiserId` | object |  |
| `onlineBookings.adroll.pixelId` | object |  |
| `onlineBookings.allowBookingsDaysInAdvance` | number |  |
| `onlineBookings.allowOnlineBookingsTimeZoneChoice` | boolean |  |
| `onlineBookings.bookingReservationMinutes` | number |  |
| `onlineBookings.calendarInfo` | object |  |
| `onlineBookings.dailyBookingsLimit` | number |  |
| `onlineBookings.disabledText` | object |  |
| `onlineBookings.disabledTitle` | object |  |
| `onlineBookings.enabled` | boolean |  |
| `onlineBookings.googleAnalytics.trackingId` | object |  |
| `onlineBookings.googleTagManager.containerId` | object |  |
| `onlineBookings.logoUrl` | object |  |
| `onlineBookings.maxAppointmentsPerDaySegment` | number |  |
| `onlineBookings.minHoursAdvanceRequiredToBook` | number |  |
| `onlineBookings.minHoursNoticeForPatientCancellation` | number |  |
| `onlineBookings.noticeEnabled` | boolean |  |
| `onlineBookings.noticeText` | object |  |
| `onlineBookings.noticeTitle` | object |  |
| `onlineBookings.notifyPractitionerByEmail` | boolean |  |
| `onlineBookings.notifyPractitionerBySms` | boolean |  |
| `onlineBookings.policy` | object |  |
| `onlineBookings.practitionerOrder` | object |  |
| `onlineBookings.privacyPolicyUrl` | object |  |
| `onlineBookings.requirePatientAddress` | boolean |  |
| `onlineBookings.showAppointmentDuration` | boolean |  |
| `onlineBookings.showPrices` | boolean |  |
| `onlinePayments.activated` | boolean |  |
| `patientCustomFieldsDefinition` | object |  |
| `patientPrivacy.anonymiseAppointmentsOnDeletion` | boolean |  |
| `patientPrivacy.anonymiseBookingNotifications` | boolean |  |
| `patientPrivacy.anonymiseInvoicesAndPaymentsOnDeletion` | boolean |  |
| `patientPrivacy.baaRequested` | boolean |  |
| `patientPrivacy.browserTitleNameFormat` | string |  |
| `patientPrivacy.icalPatientNameOption` | string |  |
| `patientPrivacy.preventSendingFinancialDataByEmail` | boolean |  |
| `patientPrivacy.requiresHipaaCompliance` | boolean |  |
| `reminders.defaultRemindersCommunicationChannels[]` | number |  |
| `reminders.defaultRemindersCommunicationChannelsDescription` | string |  |
| `reminders.defaultReminderType` | string |  |
| `sms.alphanumericSourceNumberRequired` | boolean |  |
| `sms.defaultAlphanumericSourceNumber` | string |  |
| `sms.maxMessageLength` | object |  |
| `sms.numberOfUsableCharactersPerMessage` | number |  |
| `sms.repliesSupported` | boolean |  |
| `terminology.addressCity` | string |  |
| `terminology.addressPostCode` | string |  |
| `terminology.addressState` | string |  |
| `terminology.patient` | string |  |
| `terminology.titles[]` | string |  |
| `waitList.defaultWaitListExpiryPeriod` | number |  |

## Native endpoint

Through the native Cliniko API, this operation is `GET /settings` (base URL `https://api.au5.cliniko.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-settings.md) for the provider-specific parameters and requirements.

