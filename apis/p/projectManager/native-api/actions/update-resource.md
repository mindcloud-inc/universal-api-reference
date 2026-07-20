# Update Resource with ProjectManager

Updates an existing resource in ProjectManager.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/data/resources/:resourceId`
- **Base URL:** `https://api.projectmanager.com`
- **Official documentation:** [Update Resource](https://developer.projectmanager.com/api-reference/resource/update-resource)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resourceId` | path | `string` | yes | The id of the resource |
| `firstName` | body | `string` | no | The first name of the person Resource.              Applies to personnel Resources only. |
| `lastName` | body | `string` | no | The last name of the person Resource.              Applies to personnel Resources only. |
| `email` | body | `string` | no | The email address of this Resource.              Note that this email cannot be changed once it has been assigned. |
| `hourlyRate` | body | `number` | no | The basic hourly rate for this Resource. |
| `phone` | body | `string` | no | The phone number associated with this Resource. |
| `city` | body | `string` | no | The city where this Resource is located. |
| `state` | body | `string` | no | The state or region where this Resource is located.  This value is not constrained to a list of known states or regions. |
| `countryCode` | body | `string` | no | A text field indicating the country in which this Resource is located. This value must be one of the following: US, NZ, AU. |
| `notes` | body | `string` | no | Free-form text notes about this Resource.  You may use this field to store extra information about the Resource. |
| `roleId` | body | `string` | no | The Role Id associated with this Resource.              Applies to personnel Resources only. |
| `teamIds[]` | body | `array<string>` | no | The list of ResourceTeams to which this Resource belongs. |
| `teamIds[]` | body | `array<string>` | no | The list of ResourceTeams to which this Resource belongs. |
| `teamIds[]` | body | `array<string>` | no | The list of ResourceTeams to which this Resource belongs. |
| `skillIds[]` | body | `array<string>` | no | The list of ResourceSkills possessed by this Resource. |
| `skillIds[]` | body | `array<string>` | no | The list of ResourceSkills possessed by this Resource. |
| `skillIds[]` | body | `array<string>` | no | The list of ResourceSkills possessed by this Resource. |
| `isActive` | body | `boolean` | no | Active/Inactive the Resource. |
| `approverId` | body | `string` | no | The Approver Id associated with this Resource.              Applies to personnel Resources only. |
| `colorName` | body | `string` | no | Collaboration Color for this resource.              eg. teal, cyan, lightblue, blurple, purple, pink, orange, gray |
| `language` | body | `string` | no | Translation Language for this resource.              e.g. en-US, en-GB, fr-FR, es-ES |
