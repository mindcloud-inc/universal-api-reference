# Update Person with OfficeMaps

Updates an existing person in OfficeMaps.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/person/:id`
- **Base URL:** `https://api.officemaps.io`
- **Official documentation:** [Update Person](https://api.officemaps.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `badgeNumber` | body | `string` | no | Badge number. |
| `calendarViewId` | body | `number` | no | OfficeMaps calendar view ID. |
| `cell` | body | `string` | no | Person mobile number. |
| `directReports[]` | body | `array<string>` | no | List of direct report person IDs. |
| `displayName` | body | `string` | no | Preferred display name. |
| `email` | body | `string` | no | Person email address. |
| `employeeId` | body | `string` | no | External employee ID. |
| `facebookProfile` | body | `string` | no | Facebook profile URL. |
| `firstName` | body | `string` | no | Person first name. |
| `id` | path | `string` | yes | Person UUID. |
| `initials` | body | `string` | no | Person initials. |
| `isAllowOTPLogin` | body | `boolean` | no | Allow one-time-password login. |
| `isExcludeFromStatusNotifications` | body | `boolean` | no | Exclude from status notifications. |
| `isHiddenFromUsers` | body | `boolean` | no | Hide the person from users. |
| `lastName` | body | `string` | no | Person last name. |
| `linkedInProfile` | body | `string` | no | LinkedIn profile URL. |
| `personStatusComment` | body | `string` | no | Temporary status comment. |
| `personStatusExpiry` | body | `date` | no | Status expiry timestamp. |
| `personTypeId` | body | `number` | no | OfficeMaps person type ID. |
| `phone` | body | `string` | no | Person phone number. |
| `phoneExtension` | body | `string` | no | Person phone extension. |
| `position` | body | `string` | no | Person position or role. |
| `profileBlurb` | body | `string` | no | Profile blurb. |
| `reportsTo[]` | body | `array<string>` | no | List of manager person IDs. |
| `skypeName` | body | `string` | no | Skype name. |
| `title` | body | `string` | no | Person title. |
| `twitterProfile` | body | `string` | no | Twitter profile URL. |
| `username` | body | `string` | no | Person user name. |
| `webPage` | body | `string` | no | Personal or company web page. |
