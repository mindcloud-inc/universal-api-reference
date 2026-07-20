# Create Person with OfficeMaps

Creates a new person in OfficeMaps.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/person`
- **Base URL:** `https://api.officemaps.io`
- **Official documentation:** [Create Person](https://api.officemaps.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `badgeNumber` | body | `string` | no | Badge number. |
| `displayName` | body | `string` | no | Preferred display name. |
| `doNotSendNewPasswordEmail` | body | `boolean` | no | Skip the new password email. |
| `email` | body | `string` | no | Person email address. |
| `employeeId` | body | `string` | no | External employee ID. |
| `firstName` | body | `string` | no | Person first name. |
| `isAllowOTPLogin` | body | `boolean` | no | Allow one-time-password login. |
| `isExcludeFromStatusNotifications` | body | `boolean` | no | Exclude from status notifications. |
| `isHiddenFromUsers` | body | `boolean` | no | Hide the person from users. |
| `lastName` | body | `string` | no | Person last name. |
| `personTypeId` | body | `number` | no | OfficeMaps person type ID. |
| `phone` | body | `string` | no | Person phone number. |
| `phoneExt` | body | `string` | no | Person phone extension. |
| `position` | body | `string` | no | Person position or role. |
| `timezoneId` | body | `string` | no | Timezone UUID. |
| `userName` | body | `string` | no | Person user name. |
