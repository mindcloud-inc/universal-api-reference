# Create Job with Workiz

Creates a new job in Workiz.

## Endpoint

- **Method:** `POST`
- **Path:** `/job/create/`
- **Base URL:** `https://api.workiz.com/api/v1/{apiKey}`
- **Official documentation:** [Create Job](https://developer.workiz.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Address` | body | `string` | no | Street address. |
| `City` | body | `string` | no | City. |
| `ClientId` | body | `number` | no | Existing Workiz client ID. |
| `Company` | body | `string` | no | Company name. |
| `Country` | body | `string` | no | Country code or name. |
| `Email` | body | `string` | no | Customer email address. |
| `FirstName` | body | `string` | no | Customer first name. |
| `JobDateTime` | body | `string` | no | Job start date and time. |
| `JobEndDateTime` | body | `string` | no | Job end date and time. |
| `JobNotes` | body | `string` | no | Job notes. |
| `JobSource` | body | `string` | no | Job source. |
| `JobType` | body | `string` | no | Job type. |
| `LastName` | body | `string` | no | Customer last name. |
| `Phone` | body | `string` | no | Primary phone number. |
| `PhoneExt` | body | `string` | no | Primary phone extension. |
| `PostalCode` | body | `string` | no | Postal code. |
| `ReferralCompany` | body | `string` | no | Referral company. |
| `SecondPhone` | body | `string` | no | Secondary phone number. |
| `SecondPhoneExt` | body | `string` | no | Secondary phone extension. |
| `ServiceArea` | body | `string` | no | Service area. |
| `State` | body | `string` | no | State or region. |
| `Timezone` | body | `string` | no | Job timezone. |
| `Unit` | body | `string` | no | Unit, suite, or apartment. |
