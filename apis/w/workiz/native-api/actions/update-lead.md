# Update Lead with Workiz

Updates an existing lead in Workiz.

## Endpoint

- **Method:** `POST`
- **Path:** `/lead/update/`
- **Base URL:** `https://api.workiz.com/api/v1/{apiKey}`
- **Official documentation:** [Update Lead](https://developer.workiz.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Address` | body | `string` | no | Street address. |
| `City` | body | `string` | no | City. |
| `ClientId` | body | `number` | no | Existing Workiz client ID. |
| `Company` | body | `string` | no | Company name. |
| `Country` | body | `string` | no | Country code or name. |
| `Email` | body | `string` | no | Lead email address. |
| `FirstName` | body | `string` | no | Lead first name. |
| `JobSource` | body | `string` | no | Lead source. |
| `JobType` | body | `string` | no | Lead job type. |
| `LastName` | body | `string` | no | Lead last name. |
| `LeadDateTime` | body | `string` | no | Lead start date and time. |
| `LeadEndDateTime` | body | `string` | no | Lead end date and time. |
| `LeadNotes` | body | `string` | no | Lead notes. |
| `Phone` | body | `string` | no | Primary phone number. |
| `PhoneExt` | body | `string` | no | Primary phone extension. |
| `PostalCode` | body | `string` | no | Postal code. |
| `SecondPhone` | body | `string` | no | Secondary phone number. |
| `SecondPhoneExt` | body | `string` | no | Secondary phone extension. |
| `ServiceArea` | body | `string` | no | Service area. |
| `State` | body | `string` | no | State or region. |
| `Status` | body | `string` | no | Lead status. |
| `Tags[]` | body | `array<string>` | no | Lead tags. |
| `Timezone` | body | `string` | no | Lead timezone. |
| `Unit` | body | `string` | no | Unit, suite, or apartment. |
| `UUID` | body | `string` | yes | The lead UUID to update. |
