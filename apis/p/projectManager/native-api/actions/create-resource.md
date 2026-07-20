# Create Resource with ProjectManager

Creates a new resource in ProjectManager.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/data/resources`
- **Base URL:** `https://api.projectmanager.com`
- **Official documentation:** [Create Resource](https://developer.projectmanager.com/api-reference/resource/create-resource)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `firstName` | body | `string` | yes | The first name of the person Resource.              Applies to personnel Resources only. |
| `lastName` | body | `string` | no | The last name of the person Resource.              Applies to personnel Resources only. |
| `email` | body | `string` | no | The email address of this Resource. |
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
| `colorName` | body | `string` | no | Collaboration Color for this resource.              eg. teal, cyan, lightblue, blurple, purple, pink, orange, gray |
| `language` | body | `string` | no | Language code for this Resource. |
| `country` | body | `string` | no | Deprecated - this property is no longer being used.  Please pass in Country data on the CountryCode property.              A text field indicating the country in which this Resource is located.  This value is not constrained to the list of known ISO 3166 country names or codes. |
| `role` | body | `string` | no | Deprecated - this property is no longer being used.  Please pass in Role data on the RoleId property              The Role privileges associated with this Resource.              Applies to personnel Resources only. |
| `teams[]` | body | `array<string>` | no | Deprecated - this property is no longer being used.  Please pass in Team data on the TeamIds property              The list of ResourceTeams to which this Resource belongs. |
| `teams[]` | body | `array<string>` | no | Deprecated - this property is no longer being used.  Please pass in Team data on the TeamIds property              The list of ResourceTeams to which this Resource belongs. |
| `teams[]` | body | `array<string>` | no | Deprecated - this property is no longer being used.  Please pass in Team data on the TeamIds property              The list of ResourceTeams to which this Resource belongs. |
| `skills[]` | body | `array<string>` | no | Deprecated - this property is no longer being used.  Please pass in Skill data on the SkillIds property              The list of ResourceSkills possessed by this Resource. |
| `skills[]` | body | `array<string>` | no | Deprecated - this property is no longer being used.  Please pass in Skill data on the SkillIds property              The list of ResourceSkills possessed by this Resource. |
| `skills[]` | body | `array<string>` | no | Deprecated - this property is no longer being used.  Please pass in Skill data on the SkillIds property              The list of ResourceSkills possessed by this Resource. |
