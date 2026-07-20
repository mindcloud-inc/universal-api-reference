# Submit Person Feedback with LeadIQ

## Endpoint

- **Method:** `POST`
- **Path:** `graphql`
- **Base URL:** `https://api.leadiq.com/`
- **Official documentation:** [Submit Person Feedback](https://developer.leadiq.com/#mutation-submitPersonFeedback)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.input.personId` | body | `string` | no | LeadIQ person identifier for the contact you are reporting feedback about. |
| `variables.input.value` | body | `string` | yes | The corrected email address or phone number value you are submitting feedback for. |
| `variables.input.status` | body | `list` | no | Contact info status. Allowed values: Correct or Invalid. Accepted values: `Correct`, `Invalid`. |
| `variables.input.type` | body | `list` | no | Contact info type. Common values include WorkEmail, WorkPhone, PersonalEmail, and PersonalPhone. Accepted values: `Fax`, `PersonalEmail`, `PersonalLandline`, `PersonalMobile`, `PersonalPhone`, `WorkBranch`, `WorkEmail`, `WorkHQ`, `WorkMobile`, `WorkPhone`. |
| `variables.input.linkedinUrl` | body | `string` | no | LinkedIn profile URL for the person you are reporting feedback about. |
| `variables.input.linkedinId` | body | `string` | no | LinkedIn member ID for the person you are reporting feedback about. |
| `variables.input.name` | body | `string` | no | Name of the person the feedback refers to. |
| `variables.input.companyId` | body | `string` | no | LeadIQ company identifier associated with the person. |
| `variables.input.companyName` | body | `string` | no | Company name associated with the person. |
| `variables.input.companyDomain` | body | `string` | no | Company domain associated with the person. |
| `variables.input.title` | body | `string` | no | Job title associated with the person. |
| `variables.input.invalidReason` | body | `string` | no | Reason the value is invalid. Use one of LeadIQ's InvalidReason enum values such as WrongPerson or Other. |
| `variables.input.lastSeen` | body | `date` | no | When the contact value was last seen, as an ISO date-time. |
