# Zenoti: Get Guest Details



```
GET https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/get-guest-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenoti `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/get-guest-details?connectionId=$CONNECTION_ID&guestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "guestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/get-guest-details?${params}`, {
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
      "additionalDetails": "string",
      "addressInfo": "string",
      "canEditPersonalInfo": true,
      "centerId": "string",
      "centerName": "Ava Chen",
      "code": "string",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "depositApplicability": {
        "isDepositApplicable": true
      },
      "guestMilestoneDetails": "string",
      "guestPasses": "string",
      "id": "string",
      "isGuestCustomFormFilled": true,
      "isOnlineBookingBlocked": true,
      "isVirtualGuest": true,
      "offlineId": "string",
      "personalInfo": {
        "anniversaryDate": "2026-05-07T12:00:00.000Z",
        "dateOfBirth": "2026-05-07T12:00:00.000Z",
        "dobIncompleteYear": "string",
        "email": "ava@example.com",
        "firstName": "Ava",
        "gender": 1,
        "genderName": "Ava Chen",
        "homePhone": "string",
        "isMinor": true,
        "languageId": 1,
        "lastName": "Chen",
        "lockGuestCustomData": true,
        "middleName": "Ava Chen",
        "mobilePhone": {
          "countryCode": 1,
          "number": "string",
          "phoneCode": 1
        },
        "nationalityId": 1,
        "pan": "string",
        "userName": "Ava Chen",
        "workPhone": "string"
      },
      "preferences": "string",
      "preferredServiceId": "string",
      "primaryEmployee": "string",
      "referral": "string",
      "tags": "string",
      "validateAdditionalDetails": true,
      "validateAdditionalDetails2": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `additionalDetails` | string |  |
| `addressInfo` | string |  |
| `canEditPersonalInfo` | boolean |  |
| `centerId` | string |  |
| `centerName` | string |  |
| `code` | string |  |
| `createdDate` | date |  |
| `depositApplicability.isDepositApplicable` | boolean |  |
| `guestMilestoneDetails` | string |  |
| `guestPasses` | string |  |
| `id` | string |  |
| `isGuestCustomFormFilled` | boolean |  |
| `isOnlineBookingBlocked` | boolean |  |
| `isVirtualGuest` | boolean |  |
| `offlineId` | string |  |
| `personalInfo.anniversaryDate` | date |  |
| `personalInfo.dateOfBirth` | date |  |
| `personalInfo.dobIncompleteYear` | string |  |
| `personalInfo.email` | string |  |
| `personalInfo.firstName` | string |  |
| `personalInfo.gender` | number |  |
| `personalInfo.genderName` | string |  |
| `personalInfo.homePhone` | string |  |
| `personalInfo.isMinor` | boolean |  |
| `personalInfo.languageId` | number |  |
| `personalInfo.lastName` | string |  |
| `personalInfo.lockGuestCustomData` | boolean |  |
| `personalInfo.middleName` | string |  |
| `personalInfo.mobilePhone.countryCode` | number |  |
| `personalInfo.mobilePhone.number` | string |  |
| `personalInfo.mobilePhone.phoneCode` | number |  |
| `personalInfo.nationalityId` | number |  |
| `personalInfo.pan` | string |  |
| `personalInfo.userName` | string |  |
| `personalInfo.workPhone` | string |  |
| `preferences` | string |  |
| `preferredServiceId` | string |  |
| `primaryEmployee` | string |  |
| `referral` | string |  |
| `tags` | string |  |
| `validateAdditionalDetails` | boolean |  |
| `validateAdditionalDetails2` | string |  |

## Native endpoint

Through the native Zenoti API, this operation is `GET guests/:guestId` (base URL `https://api.zenoti.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-guest-details.md) for the provider-specific parameters and requirements.

