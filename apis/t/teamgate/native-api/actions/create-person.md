# Create Person with Teamgate

Creates a new person in Teamgate.

## Endpoint

- **Method:** `POST`
- **Path:** `/people`
- **Base URL:** `https://api.teamgate.com/v4`
- **Official documentation:** [Create Person](https://developers.teamgate.com/#6a612101-c0cb-404c-9442-29d07c352185)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Person name. |
| `companyId` | body | `string` | no | Existing company ID to link to the person. |
| `jobTitle` | body | `string` | no | Person job title. |
| `customerStatusId` | body | `string` | no | Customer status ID. |
| `prospectStatusId` | body | `string` | no | Prospect status ID. |
| `starred` | body | `string` | no | Whether the person is starred. Use Teamgate values like yes or no. |
| `ownerId` | body | `string` | no | Owner user ID. |
| `source` | body | `string` | no | Person source name. |
| `sourceDescription` | body | `string` | no | Person source description. |
| `industry` | body | `string` | no | Person industry name. |
| `industryDescription` | body | `string` | no | Person industry description. |
| `tags` | body | `string` | no | Person tags. |
